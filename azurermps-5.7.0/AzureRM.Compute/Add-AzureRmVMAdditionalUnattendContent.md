---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
ms.openlocfilehash: 0c823dd974fd2d01c7502c4cf45e67769e442526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576624"
---
# Add-AzureRmVMAdditionalUnattendContent

## Sammanfattning
Lägger till information i svars filen för obevakad Windows-installation.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmVMAdditionalUnattendContent** lägger till information i svars filen för obevakad Windows-installation.
Ange ytterligare Base 64-kodad. XML-formaterad information som läggs till i unattend.xml-filen.

## BESKRIVS

### Exempel 1: lägga till innehåll i unattend.xml
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzureRmVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.

Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.
Kommandot tilldelar den virtuella datorn ett namn och en storlek.
Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.

Det tredje kommandot skapar ett Credential-objekt med hjälp av Get-Credential cmdlet och lagrar sedan resultatet i $Credential-variabeln.
Kommandot frågar efter användar namn och lösen ord.
Om du vill ha mer information skriver du `Get-Help Get-Credential` .

Det fjärde kommandot använder cmdleten **set-AzureRmVMOperatingSystem** för att konfigurera den virtuella datorn som lagras i $VirtualMachine.

Det femte kommandot tilldelar innehåll till $AucContent variabel.
Innehållet inkluderar ett lösen ord.

Med kommandot slut läggs innehållet som lagras i $AucContent till unattend.xml-filen.

## MALLPARAMETRAR

### -Innehåll
Anger Base 64-kodat XML-formaterat innehåll.
Denna cmdlet lägger till innehållet i unattend.xml-filen.
XML-innehåll måste vara mindre än 4 KB och måste innehålla rot elementet för den inställning eller funktion som denna cmdlet infogar.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SettingName
Anger namnet på den inställning som innehållet gäller för.
De acceptabla värdena för den här parametern är:

- FirstLogonCommands
- Automatisk inloggning

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Anger det virtuella dator objekt som denna cmdlet ändrar.
Använd cmdleten [Get-AzureRmVM](./Get-AzureRmVM.md) för att hämta ett virtuellt dator objekt.
Skapa ett virtuellt dator objekt med hjälp av [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmAvailabilitySet](./Get-AzureRmAvailabilitySet.md)

[Set-AzureRmVMOperatingSystem](./Set-AzureRmVMOperatingSystem.md)

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)
