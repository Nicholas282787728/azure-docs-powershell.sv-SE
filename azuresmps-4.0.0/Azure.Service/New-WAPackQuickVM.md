---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100630"
---
# New-WAPackQuickVM

## Sammanfattning
Skapar en virtuell dator baserad på en mall.

## FRÅGESYNTAXEN

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
De här ämnena är föråldrade och kommer att tas bort i framtiden.
I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.
För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .

Cmdleten **New-WAPackQuickVM** skapar en virtuell dator baserad på en mall.

## BESKRIVS

### Exempel 1: skapa en virtuell dator baserad på en mall
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

Det första kommandot skapar ett **PSCredential** -objekt och lagrar det sedan i $credentials variabel.
Du uppmanas att ange ett konto och lösen ord.
Om du vill ha mer information skriver du `Get-Help Get-Credential` .

Det andra kommandot får en mall med cmdleten **Get-WAPackVMTemplate** .
Kommandot anger ID för en mall.
Kommandot lagrar mallnamnet i $TemplateID variabel.

Med kommandot slut skapas en virtuell dator med namnet VirtualMachine023.
Kommandot baserar den virtuella datorn på mallen som lagras i $TemplateId.

## MALLPARAMETRAR

### -Namn
Anger ett namn för den virtuella datorn.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Mall
Anger en mall.
Cmdleten skapar en virtuell dator utifrån den mall som du anger.
Använd cmdleten **Get-WAPackVMTemplate** för att få ett Template-objekt.

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
Anger autentiseringsuppgifter för det lokala administratörs kontot.
Om du vill hämta ett **PSCredential** -objekt använder du cmdleten **Get-Credential** .
Om du vill ha mer information skriver du `Get-Help Get-Credential` .

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-WAPackVM](./New-WAPackVM.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)


