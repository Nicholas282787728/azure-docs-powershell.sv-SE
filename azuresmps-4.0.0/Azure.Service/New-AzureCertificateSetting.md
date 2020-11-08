---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099162"
---
# New-AzureCertificateSetting

## Sammanfattning
Skapar ett objekt för ett certifikat i en tjänst.

## FRÅGESYNTAXEN

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureCertificateSetting** skapar ett objekt för ett certifikat i en Azure-tjänst.

Du kan använda ett certifikat inställnings objekt för att skapa ett konfigurations objekt med hjälp av cmdleten **Add-AzureProvisioningConfig** .
Använd ett konfigurations objekt för att skapa en virtuell dator med cmdleten **New-AzureVM** .
Du kan använda ett certifikat inställnings objekt för att skapa en virtuell dator med cmdleten **New-AzureQuickVM** .

## BESKRIVS

### Exempel 1: skapa ett objekt för certifikat inställning
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

Det här kommandot skapar ett objekt för en inställning för ett befintligt certifikat.

### Exempel 2: skapa en virtuell dator som använder ett konfigurations inställnings objekt
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

Det första kommandot lägger till certifikatet ContosoCert. cer till tjänsten som heter ContosoService genom att använda cmdleten **Add-AzureCertificate** .

Det andra kommandot skapar ett objekt för en inställning för certifikat och lagrar det sedan i $CertificateSetting variabel.

Det tredje kommandot får en bild från bild databasen med cmdleten **Get-AzureVMImage** .
Det här kommandot lagrar bilden i variabeln $Image.

Med kommandot slut skapas ett konfigurations objekt för virtuell dator baserat på bilden i $Image genom att använda cmdleten **New-AzureVMConfig** .
Kommandot skickar det objektet till cmdleten **Add-AzureProvisioningConfig** med hjälp av pipeline-operatorn.
Denna cmdlet lägger till konfigurations information till konfigurationen.
Kommandot skickar objektet till cmdleten **New-AzureVM** , vilket skapar den virtuella datorn.

## MALLPARAMETRAR

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

### -Butiks namn
Anger certifikat arkivet där certifikatet ska placeras.
Giltiga värden är: 

- Adress boks
- AuthRoot
- CertificateAuthority
- Är inte tillåtna
- Kalendern
- Enhet
- TrustedPeople
- TrustedPublisher

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tumavtryck
Anger tumavtryck för certifikatet.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureCertificate](./Add-AzureCertificate.md)

[Add-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Get-AzureCertificate](./Get-AzureCertificate.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[New-AzureQuickVM](./New-AzureQuickVM.md)

[New-AzureVM](./New-AzureVM.md)

[Remove-AzureCertificate](./Remove-AzureCertificate.md)


