---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099185"
---
# Set-AzurePublicIP

## Sammanfattning
Lägger till en offentlig IP-adress till en virtuell Azure-dator.

## FRÅGESYNTAXEN

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzurePublicIP** lägger till en offentlig IP-adress till en virtuell Azure-dator.
Om du kör denna cmdlet för en befintlig virtuell dator uppdaterar du den virtuella datorn för att genomföra ändringarna.
Du kan ange en domän namns etikett för att skapa en motsvarande DNS-post för den offentliga IP-adressen.

## BESKRIVS

### Exempel 1: lägga till en offentlig IP för en befintlig virtuell dator
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

Det här kommandot får den virtuella datorn som heter FTPInstance i tjänsten FTPInAzure med hjälp av cmdleten **Get-AzureVM** .
Kommandot skickar den virtuella datorn till den aktuella cmdleten med operatören.
Den aktuella cmdleten lägger till det offentliga IP-namnet ftpip.
Kommandot skickar den virtuella datorn till cmdleten **Update-AzureVM** som implementerar dina ändringar.

### Exempel 2: lägga till en offentlig IP-adress på en ny virtuell dator
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

Det här kommandot skapar ett konfigurations objekt för virtuell dator med hjälp av cmdleten **New-AzureVMConfig** .
Kommandot skickar det objektet till cmdleten **Add-AzureProvisioningConfig** , som ger ytterligare konfiguration.
Den aktuella cmdleten lägger till det offentliga IP-namnet ftpip.
Kommandot överför konfigurationen till cmdleten **New-AzureVM** , som skapar den virtuella datorn.

### Exempel 3: lägga till en offentlig IP och etikett till en befintlig virtuell dator
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

Det här kommandot får den virtuella datorn som heter FTPInstance i tjänsten FTPInAzure med hjälp av cmdleten **Get-AzureVM** .
Kommandot skickar den virtuella datorn till den aktuella cmdleten med operatören.
Den aktuella cmdleten lägger till det offentliga IP-namnet ftpip och Label ipname.
Kommandot uppdaterar den virtuella datorn som implementerar dina ändringar.

### Exempel 4: lägga till en offentlig IP och etikett på en ny virtuell dator
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

Det här kommandot skapar ett konfigurations objekt för virtuell dator och skickar sedan objektet till **Add-AzureProvisioningConfig** , vilket ger ytterligare konfiguration.
Den aktuella cmdleten lägger till det offentliga IP-namnet ftpip och Label ipname.
Kommandot skapar den virtuella datorn.

## MALLPARAMETRAR

### -DomainNameLabel
Anger det namn som ska användas för en motsvarande DNS-post för den offentliga IP-adressen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
Anger tids gräns för TCP-timeout i minuter.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

### -PublicIPName
Anger det offentliga IP-namnet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Anger den virtuella dator där denna cmdlet lägger till offentlig IP.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. WindowsAzure. kommandon. ServiceManagement. Model. IPersistentVM

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzurePublicIP](./Get-AzurePublicIP.md)

[Get-AzureVM](./Get-AzureVM.md)

[New-AzureVM](./New-AzureVM.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)

[Remove-AzurePublicIP](./Remove-AzurePublicIP.md)

[Update-AzureVM](./Update-AzureVM.md)


