---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099612"
---
# Add-AzureProvisioningConfig

## Sammanfattning
Lägger till etableringen-konfiguration för en virtuell Azure-dator.

## FRÅGESYNTAXEN

### Windows (standard)
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### WindowsDomain
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureProvisioningConfig** lägger till konfigurations information för etableringen i en konfiguration för en Azure-dator.
Du kan använda konfigurationsobjektet för att skapa en virtuell dator.

Denna cmdlet har stöd för olika konfigurations konfigurationer, inklusive fristående Windows-servrar, Windows-servrar som är anslutna till en Active Directory-domän och Linux-baserade servrar.

Om du vill skapa en server för Active Directory-anslutare anger du det fullständigt kvalificerade domän namnet för Active Directory-domänen och domänautentiseringsuppgifter för en användare som har behörighet att ansluta den virtuella datorn till domänen.

## BESKRIVS

### Exempel 1: skapa en fristående virtuell dator
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

Det här kommandot skapar ett konfigurations objekt för virtuell dator med hjälp av cmdleten **New-AzureVMConfig** .
Kommandot skickar detta objekt till den aktuella cmdleten med hjälp av pipeline-operatorn.
Den aktuella cmdleten lägger till etableringen konfiguration för en virtuell dator som kör operativ systemet Windows.
Konfigurationen inkluderar administratörens användar namn och lösen ord.
Kommandot överför konfigurationen till cmdleten **New-AzureVM** , som skapar den virtuella datorn.

### Exempel 2: skapa en domänansluten virtuell dator
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

Det här kommandot skapar ett konfigurations objekt för virtuell dator och skickar det sedan till den aktuella cmdleten.
Den aktuella cmdleten lägger till etableringen konfiguration för en virtuell dator som ska kopplas till domänen contoso.
Kommandot innehåller användar namn och lösen ord som krävs för att ansluta den virtuella datorn till domänen.
Konfigurationen kräver att användaren ändrar lösen ordet vid första inloggningen.
Kommandot skapar den virtuella datorn baserat på det etablerings objekt som du använder.

### Exempel 3: skapa en Linux-baserad virtuell dator
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

Det här kommandot skapar ett konfigurations objekt för virtuell dator och skickar det sedan till den aktuella cmdleten.
Den aktuella cmdleten lägger till etableringen konfiguration för en virtuell dator som kör Linux-operativsystemet.
Konfigurationen inkluderar rot användar namnet och lösen ordet.
Kommandot skapar den virtuella datorn baserat på det etablerings objekt som du använder.

### Exempel 4: skapa en virtuell dator som innehåller certifikat för WinRM
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Det första kommandot får certifikat från ett certifikat Arkiv och lagrar dem sedan i $certs mat ris variabel.

Det andra kommandot skapar ett konfigurations objekt för virtuell dator och skickar det sedan till den aktuella cmdleten.
Den aktuella cmdleten lägger till etableringen med konfiguration som inkluderar certifikat för WinRM.
Kommandot skapar den virtuella datorn baserat på det etablerings objekt som du använder.

### Exempel 5: skapa en virtuell dator med WinRM aktiverat över HTTP
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Det här kommandot skapar ett konfigurations objekt för virtuell dator och skickar det sedan till den aktuella cmdleten.
Den aktuella cmdleten lägger till etableringen konfiguration med WinRM aktiverat över HTTP.
Kommandot skapar den virtuella datorn baserat på det etablerings objekt som du använder.

### Exempel 6: skapa en virtuell dator med WinRM inaktiverat över HTTPS
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Det här kommandot skapar ett konfigurations objekt för virtuell dator och skickar det sedan till den aktuella cmdleten.
Den aktuella cmdleten lägger till etableringen-konfiguration som inaktiverar WinRM via HTTPS.
Kommandot skapar den virtuella datorn baserat på det etablerings objekt som du använder.

### Exempel 7: skapa en virtuell dator utan att exportera nycklar
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Det första kommandot får certifikat från ett certifikat Arkiv och lagrar dem sedan i $certs mat ris variabel.

Det andra kommandot skapar ett konfigurations objekt för virtuell dator och skickar det sedan till den aktuella cmdleten.
Den aktuella cmdleten lägger till etableringen konfiguration för en virtuell dator som innehåller certifikat och exporterar inte privata nycklar.
Kommandot skapar den virtuella datorn baserat på det etablerings objekt som du använder.

## MALLPARAMETRAR

### -AdminUsername
Anger användar namnet på det administratörs konto som den här konfigurationen skapar på den virtuella datorn.

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Certifikat
Anger en uppsättning certifikat som denna konfiguration installerar på den virtuella datorn.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDataFile
Anger en datafil för den virtuella datorn.
Denna cmdlet kodar innehållet i filen som base64.
Filen måste vara mindre än 64 kilobyte lång.

Om gäst operativ systemet är Windows-operativsystemet sparas dessa data som en binär fil med namnet%SYSTEMDRIVE%\AzureData\CustomData.bin.

Om gäst operativ systemet är Linux skickar denna konfiguration data med hjälp av ovf-env.xml-filen.
Konfiguration kopierar filen till/var/lib/waagent-katalogen.
Agenten lagrar också base64-kodade data i/var/lib/waagent/CustomData.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAutomaticUpdates
Anger att den här konfigurationen inaktiverar automatiska uppdateringar.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableGuestAgent
Anger att den här konfigurationen inaktiverar infrastrukturen som en tjänst gäst agent (IaaS).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSSH
Anger att den här konfigurationen inaktiverar SSH.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWinRMHttps
Anger att den här konfigurationen inaktiverar Windows Remote Management (WinRM) på HTTPS.
WinRM är aktiverat som standard via HTTPS.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Domain
Anger namnet på domänen för det konto som har behörighet att lägga till datorn i en domän.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainPassword
Anger lösen ordet för det användar konto som har behörighet att lägga till datorn i en domän.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainUserName
Anger namnet på det användar konto som har behörighet att lägga till datorn i en domän.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Anger att den här konfigurationen aktiverar WinRM över HTTP.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Anger hur den här cmdleten svarar på en informations händelse.

De acceptabla värdena för den här parametern är:

- Vidare
- Över
- Inquire
- SilentlyContinue
- Stanna
- Avbryt

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Anger en informations variabel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JoinDomain
Anger det fullständigt kvalificerade domän namnet (FQDN) för domänen som ska anslutas.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
Anger att den här konfigurationen skapar en Linux-konfiguration.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinuxUser
Anger användar namnet på det administratörs konto för Linux som den här konfigurationen skapar på den virtuella datorn.

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MachineObjectOU
Anger det fullständigt kvalificerade namnet på den organisatoriska enhet (OU) som konfigurationen skapar dator kontot i.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoExportPrivateKey
Anger att den här konfigurationen inte laddar upp den privata knappen.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoRDPEndpoint
Anger att den här konfigurationen skapar en virtuell dator utan slut punkt för fjärr skrivbord.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHEndpoint
Anger att den här konfigurationen skapar en virtuell dator utan en SSH-slutpunkt.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHPassword
Anger att den här konfigurationen skapar en virtuell dator utan ett SSH-lösenord.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
Anger att den här konfigurationen inte lägger till en WinRM-slutpunkt för den virtuella datorn.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Lösen ord
Anger lösen ordet för administratörs kontot.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResetPasswordOnFirstLogon
Anger att den virtuella datorn kräver att användaren ändrar lösen ordet vid den första inloggningen.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHKeyPairs
Anger SSH-nyckelvärdena.

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHPublicKeys
Anger offentliga nycklar för SSH.

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeZone
Anger tids zonen för den virtuella datorn, till exempel Pacific standard time eller Canada Central, normal tid.

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Anger ett virtuellt dator objekt.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Windows
Anger att den här konfigurationen skapar en fristående virtuell dator som kör operativ systemet Windows.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsDomain
Anger att den här konfigurationen skapar Windows Server som är ansluten till en Active Directory-domän.

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
Anger ett certifikat som den här konfigurationen associeras med en WinRM-slutpunkt.

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificates
Anger en matris med X509-certifikat som distribueras till en värdbaserad tjänst.

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureVM](./New-AzureVM.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)


