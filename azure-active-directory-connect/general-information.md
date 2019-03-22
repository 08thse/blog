---
title: [�����ɗL���ȍ̎���] Azure AD Connect �T�[�o�[�̑S�ʏ��
date: 2017-10-24
tags:
  - AAD Connect
  - �T�|�[�g
  - ���̎�
---

# [�����ɗL���ȍ̎���] Azure AD Connect �T�[�o�[�̑S�ʏ��

����ɂ��́AAzure & Identity �T�|�[�g �`�[���̌㓡�ł��B
 
����� Azure AD Connect �T�[�o�[�\���Ɋւ����̎�ɂ��Ă��Љ�܂��B
Azure AD Connect �Ɋւ����̂Ƃ��ɗL���ł����A�����̃g���u���ł� �gAzure AD Connect �Ń��[�U�[�������ł��Ȃ����h �̏��擾�����킹�Ă��肢���܂��B
 
<�̎���>
�ȉ��̏��� Azure AD Connect �T�[�o�[��ō̎悵�܂��B
 
1.�A�v���P�[�V���� / �V�X�e���̃C�x���g���O
2.Azure AD Connect�g���[�X ���O
3.Azure AD Connect �̍\�����
4.Azure AD Connect �̃o�[�W�������
 
<�擾�菇>
1.�A�v���P�[�V���� / �V�X�e���̃C�x���g���O
=================================
1-1. Azure AD Connect �T�[�o�[�ɊǗ��Ҍ����ɂă��O�C�����܂��B
1-2. �R�}���h �v�����v�g�����s���܂��B
1-3. �ȉ��̃R�}���h�����s���A�o�͂��ꂽ .evtx �t�@�C�����̎悵�܂��B

``cmd 
wevtutil epl system C:\SystemEvent.evtx
wevtutil epl Application C:\AppliEvent.evtx
```
 
2.Azure AD Connect �g���[�X ���O
=====================================
���L�t�H���_�[����уt�H���_�[�z���̃t�@�C���� zip �t�@�C���Ȃǂɂ܂Ƃ߂ĕۑ����܂��B

```
c:\ProgramData\AADConnect
%localappdata%\AADConnect
��: c:\Users\admin001\AppData\Local\AADConnect
```
 
3.Azure AD Connect �̍\�����
=====================================
PowerShell �ɂĈȉ��̃R�}���h���b�g�����s���A�o�͂��ꂽ�t�H���_�[����уt�@�C���� Zip �t�@�C�����ɂ܂Ƃ߂ĕۑ����܂��B

```powershell 
Get-ADSyncAutoUpgrade > c:\ADSyncAutoUpgrade.txt
(Get-ADSyncGlobalSettings).Parameters | select Name,Value > c:\ADSyncGlobalSettings.txt
Get-ADSyncScheduler > c:\ADSyncScheduler.txt
Get-ADSyncSchedulerConnectorOverride > c:\ADSyncSchedulerConnectorOverride.txt
Get-ADSyncServerConfiguration -Path c:\aadconnect
```
 
4.Azure AD Connect �̃o�[�W�������
=====================================
4-1. �R�}���h �v�����v�g���Ǘ��҂Ƃ��ċN�����āA�ȉ��̃R�}���h�����s���܂��B

```cmd
wmic product list > product.txt
```

4-2. �J�����g �f�B���N�g���� product.txt �Ƃ��ĕۑ�����܂��B
 
�����ł��ē����܂����������O�Ɏ擾���A���₢���킹�ƍ��킹�Ă��񋟂����������ƂŎ��̂悤�ȃ����b�g������܂��B
 
1.���₢���킹�ɑ΂���񓚁E�����������͂₭�ł��܂��B
2.��X�A�Č��ł��Ȃ��Ȃ�A��蔭�����̏�񂪂Ȃ����߂ɁA���̔����v����ǋy�ł��Ȃ��Ȃ�P�[�X�����点�܂��B
3.�T�|�[�g �G���W�j�A�����̎���ē�����镪�̂��������点�܂��B
4.��񂪂��邽�߁A�T�|�[�g �G���W�j�A����莖�ۂɂ��Ă��c��������Ԃł��q�l�ƃS�[���ݒ肪�ł��܂��B
 
�u�R�~���j�e�B�ɂ�����}�C�N���\�t�g�Ј��ɂ�锭����R�����g�́A�}�C�N���\�t�g�̐����Ȍ����܂��̓R�����g�ł͂���܂���B�v
���{���̓��e�i�Y�t�����A�����N��Ȃǂ��܂ށj�́A�쐬�����_�ł̂��̂ł���A�\���Ȃ��ύX�����ꍇ������܂��B