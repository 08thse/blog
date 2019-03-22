---
title: [�����ɗL���ȍ̎���] Azure AD Connect �Ń��[�U�[�������ł��Ȃ����
date: 2017-10-24
tags:
  - AAD Connect
  - �T�|�[�g
  - ���̎�
---

# [�����ɗL���ȍ̎���] Azure AD Connect �Ń��[�U�[�������ł��Ȃ����

����ɂ��́AAzure & Identity �T�|�[�g �`�[���̌㓡�ł��B
 
����� Azure AD Connect �T�[�o�[�Ń��[�U�[�����ɖ�肪�����Ă���P�[�X�ɂ��Ď擾����������Љ�܂��B
�Ȃ��A���̏��� �g���[�U�[�����g���u���h �ɓ������Ă��܂��̂ŁA�����ĕʓr�Љ�Ă��܂� Azure AD Connect �̑S�ʏ��̍̎�����肢���܂��B
 
<�̎���>
1.�I���v���~�X Active Directory �Ɋi�[����郆�[�U�[ �I�u�W�F�N�g���
2.Azure AD Connect �T�[�o�[��̃��[�U�[ �I�u�W�F�N�g���
3.Synchronization Service Manager �̃G���[��ʃV���b�g
4.�C�x���g���O
5.�G���[���O�̏o�͌���
 
<�擾�菇>
�I���v���~�X Active Directory �Ɋi�[����郆�[�U�[ �I�u�W�F�N�g���
=================================
�����ł��Ȃ��Ƃ�����肪�ꕔ�̃I�u�W�F�N�g�Ő����Ă���ꍇ�ɂ́A����ɓ������������Ă��郆�[�U�[�Ɠ����ɖ�肪�����Ă�����̂ɂ��ď��Ȃ��Ƃ� 1 ����C�ӂɑI���̏�A�擾���������B
 
1-1. �h���C�� �R���g���[���[�ɂĊǗ��Ҍ����ŃR�}���h �v�����v�g���J���܂��B
1-2. �ȉ��̃R�}���h�����ꂼ��̃I�u�W�F�N�g�ɑ΂��Ď��s���܂��B

```cmd
ldifde.exe -f <�o�̓t�@�C����> -t 3268 -d <�����ł��Ȃ����[�U�[�� DN ��> -p subtree
```

���[�U�[�� DN ���́A���̑Ώۂ����[�U�[�̏ꍇ�ł���΁A�R�}���h�� dsquery user -name <���[�U�[��> �Ŋm�F�ł��܂��B
 
�Ⴆ�� contoso.com �h���C���� OU1 �Ƃ��� OU �ɏ������Ă��� user1 �Ƃ����A�J�E���g�̏ꍇ�ɂ́A dsquery user -name user1 �̃R�}���h�̌��ʁA���̂悤�ɕ\������܂��B

```
"CN=user1,OU=OU1,DC=contoso,DC=com"
```

���̏ꍇ�� c:\user1_ad.txt �ɏo�͂���R�}���h�͎��̂悤�ɂȂ�܂��B

```cmd 
ldifde.exe -f c:\user1_ad.txt -t 3268 -d "CN=user1,OU=OU1,DC=contoso,DC=com" -p subtree
```
 
1-3. �o�͂��ꂽ�t�@�C����ۑ����܂��B
 
2.Azure AD Connect �T�[�o�[��̃I�u�W�F�N�g���
=====================================
-  1 �̎菇�� ldifde �R�}���h�ɂĎ擾�����I�u�W�F�N�g�Ɠ��I�u�W�F�N�g�ɂ��č̎悵�܂��B
 
2-1. ����� �gC:\Program Files\Microsoft Azure AD Sync\UIShell�h �ɂ���܂� �gmiisclient.exe�h �����s���A[Synchronization Service Manager] ���J���܂��B
 
2-2. ��ʏ㕔�� [Metaverse Search] �{�^���������܂��B
2-3. ��ʏ㕔�� [Scope by Objects Type] ����A[person]��I�т܂��B
 
���܂�ɂ������̃��[�U�[�� [Search Results] �Ƃ��ďo�͂���A����ɍׂ����������w�肷��ꍇ�́A[Attribute] �ɑ������w�肵�A[Operator]�� "Equal" �� "Starts with(�O����v) "��I�����A[Value] �Ɍ������郆�[�U�[�̃L�[���[�h�����w�肭�������B
 
2-4. �\�����ꂽ ���[�U�[���_�u���N���b�N���܂��B
2-5. [Metaverse Object Properties]�̉�ʂ��Ђ낰�A [Attributes] �^�u�̐ݒ�S�̂�������悤�ɂ�����ŉ�ʃL���v�`�����擾���܂��B�i��ʂ��؂��ꍇ�́A�X�N���[���Ȃǂ��đS�̂̏����̎悵�܂��j
2-6. [Connectors]�^�u��I�����܂��B
2-7. [Distinguished Name] ��Azure AD �ƃI���v��AD �̓�̕\�����m�F���܂��B
2-8. ����� [Distinguished Name] �ݒ��I�����܂��B
2-9. �\�����ꂽ [Connector Space Object Properties] �̐ݒ�S�̂�������悤�ɉ�ʃL���v�`�����擾���܂��B
2-10 [Close] �������A��قǑI�����Ȃ������A��������� [Connector Space Object Properties] �ɂ��Ă���ʃL���v�`�����擾���܂��B
 
3.Synchronization Service Manager �̃G���[��ʃV���b�g
=====================================
Azure AD Connect �� Synchronization Service Manager �ɂăG���[���������Ă��邩�m�F���A�G���[�������Ă���ꍇ�ɂ͂��̉�ʏ����擾���܂��B
 
�m�F����ӏ���[Operations] ��I�����āA[Status]�� success �łȂ����̂ɂ��āA��ʉE���̃����N���N���b�N�����Ƃ��̂��ׂẲ�ʃV���b�g���̎悵�܂��B
 
4.�C�x���g ���O
=====================================
Azure AD Connect �T�[�o�[�ɊǗ��Ҍ����ŃT�C���C�����A��Ƃ����{���������B
 
4-1. �R�}���h �v�����v�g���Ǘ��҂Ƃ��ċN�����āA�ȉ��� 2 �̃R�}���h�����s���܂��B

```cmd
wevtutil epl system %UserProfile%\desktop\SysEvent.evtx
wevtutil epl Application %UserProfile%\desktop\AppEvent.evtx
```
 
4-2. �f�X�N�g�b�v�ɍ쐬���ꂽ evtx �`���̃C�x���g ���O���̎悵�܂��B
 
�G���[���O�̏o�͊m�F
=====================================
Azure AD Connect ��ŃR�}���h�v�����v�g���Ǘ��Ҍ����Ŏ��s���܂��B
<C:\Program Files\Microsoft Azure AD Sync\Bin> �ɂ���Acsexport.exe  ���g�p���āA�ȉ��� 4 �̃R�}���h�����s���܂��B

```cmd
csexport.exe "<�R�l�N�^�[ �X�y�[�X��(Azure AD)>" error_YYYYMMDD_1.xml /f:e 
 
csexport.exe "<�R�l�N�^�[ �X�y�[�X��(Azure AD)>" error_YYYYMMDD_2.xml /f:i
 
csexport.exe "<�R�l�N�^�[ �X�y�[�X��(�I���v�� AD)>" error_YYYYMMDD_3.xml /f:e 
 
csexport.exe "<�R�l�N�^�[ �X�y�[�X��(�I���v�� AD)>" error_YYYYMMDD_4.xml /f:i
```
 
���R�l�N�^�[ �X�y�[�X���ɂ��ẮASynchronization Service Manager [Operations]�� [Name] �ɕ\�����ꂽ���O�ł��B
 
�u�R�~���j�e�B�ɂ�����}�C�N���\�t�g�Ј��ɂ�锭����R�����g�́A�}�C�N���\�t�g�̐����Ȍ����܂��̓R�����g�ł͂���܂���B�v
���{���̓��e�i�Y�t�����A�����N��Ȃǂ��܂ށj�́A�쐬�����_�ł̂��̂ł���A�\���Ȃ��ύX�����ꍇ������܂��B