---
title: Microsoft Entra ID �ɕK�v�ȒʐM��G���h�|�C���g�܂Ƃ�
date: 2023-11-28 21:18
tags:
  - Entra ID
  - Network
---

# Entra ID �ɕK�v�ȃG���h�|�C���g�܂Ƃ�

����ɂ��́AAzure & Identity �T�|�[�g �`�[���̑��ł��B

����͂悭��������������� Microsoft Entra ID �������p���������ۂɕK�v�ƂȂ�G���h�|�C���g (URL/IP �A�h���X) �ɂ��Ă��ē����܂��BMicrosoft Entra ID �ɂ����Ă͔F�؂���A�J�E���g�Ǘ��A�A�J�E���g�����Ɏ���܂ŕ����̃T�[�r�X��񋟂��Ă���A�����p���������@�\�ɂ���ăA�N�Z�X��̃G���h�|�C���g���قȂ�܂��B���q�l�ɂ���ẮA�l�b�g���[�N �v���L�V�ɂČ����ɐڑ��\�ȃG���h�|�C���g (URL) ��𐧌䂳��Ă���ꍇ������A����������������s���Ă��邨�q�l�ł́A����ɃT�[�r�X�𗘗p���邽�߂ɌʂɃG���h�|�C���g (URL) ��������K�v������܂��B

�{�L���ɂ����ẮA�����_�Œ񋟂��Ă��� Microsoft Entra ID �̊e�T�[�r�X�Ɋւ��A�K�v�ƂȂ�G���h�|�C���g���L�ڂ������J�����ւ̃����N���܂Ƃ߂܂��B����ɂ��A�u�ǂ̃G���h�|�C���g�ɑ΂��ăA�N�Z�X��������΂����̂��܂Ƃ߂Ēm�肽���I�v�Ƃ��������v�]�ɂ������o������K���ł��B

> [!NOTE]
> �T�|�[�g�`�[���ɂĉ\�Ȍ���v�����ԗ��I�ȏ��̍X�V�ɓw�߂Ă���܂����A�{�L���ɂĂ��ׂĂ̏��̖ԗ����ł��Ă���킯�ł͂���܂���B�T�[�r�X�����p����G���h�|�C���g�̓h�L�������g�̍X�V�ƂƂ��ɕω�����\��������܂��B�����Ȉē��ɂ��Ă͊e���J�����Q�Ƃ����������A���ЃT�|�[�g�T�[�r�X�܂ł��₢���킹���������B

## Microsoft Entra ID �Ŋ�{�I�ɗ��p�����G���h�|�C���g

�܂����߂� Microsoft Entra ID �𗘗p���������ۂɊ�{�I�ɕK�v�ƂȂ�G���h�|�C���g�́A[Office 365 �� URL �� IP �A�h���X�͈̔�](https://learn.microsoft.com/ja-jp/microsoft-365/enterprise/urls-and-ip-address-ranges?view=o365-worldwide#microsoft-365-common-and-office-online) �ɋL�ڂ���Ă��� ID 56 , ID 59 ������ ID 125 �ɂȂ�܂��B������� Microsoft 365 �𗘗p����ۂ� Micorosft Entra ID �𗘗p����V�i���I�ōŒ���K�v�ƂȂ�G���h�|�C���g���܂Ƃ߂����̂ł��BMicrosoft Entra ID �������p���������ۂ́A�F�؂��s���N���C�A���g���炱���̃G���h�|�C���g�ɂ��ăl�b�g���[�N�̑a�ʂ��m�ۂ��������B

## Microsoft Entra ID �Ńf�o�C�X�Ǘ��ɗ��p����G���h�|�C���g

Entra ID �ł� Microsoft Entra �n�C�u���b�h�Q���AMicrosoft Entra �Q�������� Microsoft Entra �o�^�A�Ƃ��� 3 �̕��@�Ńf�o�C�X��o�^���邱�Ƃ��ł��܂��B������̕��@�𗘗p����ꍇ�ł��A[Microsoft Entra �n�C�u���b�h�Q�����\������](https://learn.microsoft.com/ja-jp/entra/identity/devices/how-to-hybrid-join#network-connectivity-requirements) �̃y�[�W�ɋL�ڂ���Ă���G���h�|�C���g�������������B

## Microsoft Entra ID �ɂė��p�K��𗘗p����G���h�|�C���g

Microsoft Entra ID �ɂė��p�K��𗘗p����ꍇ�́A[Microsoft Entra �̗��p�K��̂悭�񂹂��鎿��](https://learn.microsoft.com/ja-jp/entra/identity/conditional-access/terms-of-use#frequently-asked-questions) �̃y�[�W�ɂ��� "Q:���p�K��T�[�r�X�ɂ͂ǂ̃G���h�|�C���g���F�؂Ɏg�p����܂���?" �ɋL�ڂ���Ă���G���h�|�C���g�������������B

## Microsoft Entra Connect �Ɋ֘A����G���h�|�C���g

Microsoft Entra Connect �𗘗p���āA�n�C�u���b�h ID �\�����[�V���� (�I���v���~�X����̃A�J�E���g�̓���) �𗘗p�����ۂɕK�v�� URL �� IP �A�h���X�̈ꗗ�ɂ��Ă͏�L�́uMicrosoft Entra ID �Ŋ�{�I�ɗ��p�����G���h�|�C���g�v�̐߂��������������B�܂������āA[Microsoft Entra Connect �̐ڑ��Ɋւ�����̃g���u���V���[�e�B���O](https://learn.microsoft.com/ja-jp/entra/identity/hybrid/connect/tshoot-connect-connectivity) �̃y�[�W���Q�Ƃ������߂��܂��B�J�����K�v�ȃl�b�g���[�N �|�[�g�ƃv���g�R���ɂ��ẮA[�n�C�u���b�h ID �ŕK�v�ȃ|�[�g�ƃv���g�R��](https://learn.microsoft.com/ja-jp/entra/identity/hybrid/connect/reference-connect-ports) �̃y�[�W�ɂ�����������܂��̂ł������������B

## Microsoft Entra Connect Health Service �ɗ��p����G���h�|�C���g
 
Microsoft Entra Connect Health Service �𗘗p����ꍇ�́A[Microsoft Entra Connect Health �G�[�W�F���g�̃C���X�g�[��](https://learn.microsoft.com/ja-jp/entra/identity/hybrid/connect/how-to-connect-health-agent-install#outbound-connectivity-to-azure-service-endpoints) �y�[�W�ɋL�ڂ���Ă���G���h�|�C���g�������������B

## Microsoft Entra �A�v���P�[�V���� �v���L�V �R�l�N�^�ɂė��p�����G���h�|�C���g

Microsoft Entra �A�v���P�[�V���� �v���L�V �R�l�N�^�𗘗p�����ۂ́A[�A�v���P�[�V���� �v���L�V���g�p���ăI���v���~�X �A�v����ǉ�����](https://docs.microsoft.com/ja-jp/azure/active-directory/app-proxy/application-proxy-add-on-premises-application#prepare-your-on-premises-environment) �y�[�W�ɋL�ڂ���Ă���G���h�|�C���g�������������B


## Microsoft Entra �v���r�W���j���O �T�[�r�X�𗘗p���� IP �A�h���X�͈̔�
 
Microsoft Entra �v���r�W���j���O �T�[�r�X�͂𗘗p����ꍇ�́A[�`���[�g���A��: Microsoft Entra ID �� SCIM �G���h�|�C���g�̃v���r�W���j���O](https://learn.microsoft.com/ja-jp/entra/identity/app-provisioning/use-scim-to-provision-users-and-groups#ip-ranges) �ɋL�ڂ���Ă��� IP �A�h���X�͈̔͂��Q�Ƃ��������B

## �I���v���~�X�ɂ��� Multi-Factor Authentication Server �����p����G���h�|�C���g
 
2024 �N 9 �� 30 ���ɃT�[�r�X�̒񋟏I�����A�i�E���X������Ă��܂����A�I���v���~�X�� MFA �T�[�o�[�𗘗p����ꍇ�́A[Azure Multi-Factor Authentication Server �̃t�@�C�A�E�H�[���̗v��](https://learn.microsoft.com/ja-jp/entra/identity/authentication/howto-mfaserver-deploy#azure-multi-factor-authentication-server-firewall-requirements) �ɋL�ڂ���Ă���G���h�|�C���g�������������B

## Microsoft Private Access �p�ɃA�v���P�[�V���� �v���L�V �R�l�N�^�ɂė��p�����G���h�|�C���g

Microsoft Entra Private Access �p�ɃA�v�� �v���L�V �R�l�N�^�ɂ��ẮA[Microsoft Entra Private Access �p�ɃA�v�� �v���L�V �R�l�N�^���\��������@
](https://learn.microsoft.com/ja-jp/entra/global-secure-access/how-to-configure-connectors#allow-access-to-urls) �ɋL�ڂ���Ă���G���h�|�C���g�������������B

## Microsoft Azure �Ǘ��Z���^�[����ш�ʓI�ȃT�[�r�X�ɗ��p�����G���h�|�C���g

Microsoft Entra ID �̔F�؂ł͂Ȃ��ł����AAzure �|�[�^�����ʓI�ȃA�J�E���g �T�[�r�X�ɕK�v�ƂȂ�G���h�|�C���g�́A[�t�@�C�A�E�H�[���܂��̓v���L�V �T�[�o�[�� Azure portal �� URL ��������](https://learn.microsoft.com/ja-jp/azure/azure-portal/azure-portal-safelist-urls?tabs=public-cloud) �̃y�[�W�ɋL�ڂ���Ă���G���h�|�C���g�������������B


����AEntra ID �������p���������ۂɖ{�u���O�̓��e�������ł��Q�l�ƂȂ�܂��ƍK���ł��B
