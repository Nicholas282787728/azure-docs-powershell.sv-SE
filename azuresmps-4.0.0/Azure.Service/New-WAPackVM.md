---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100628"
---
# New-WAPackVM

## Sammanfattning
Skapar en virtuell dator.

## FRÅGESYNTAXEN

### CreateVMFromTemplate (standard)
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateLinuxVMFromTemplate
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateVMFromOSDisk
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
De här ämnena är föråldrade och kommer att tas bort i framtiden.
I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.
För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .

Cmdleten **New-WAPackVM** skapar en virtuell dator.

## BESKRIVS

### Exempel 1: skapa en virtuell dator för Windows operativ system med hjälp av en mall
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

Det första kommandot skapar ett **PSCredential** -objekt och lagrar det sedan i $credentials variabel.
Du uppmanas att ange ett konto och lösen ord.
Om du vill ha mer information skriver du `Get-Help Get-Credential` .

Det andra kommandot hämtar mallen för virtuell dator med namnet ContosoTemplate04 med hjälp av cmdleten **Get-WAPackVMTemplate** och lagrar den sedan i $Template variabel.

Med kommandot slut skapas en virtuell dator med namnet ContosoV023, baserat på mallen som lagras i $Template variabel.
Kommandot anger *Windows* -parametern och därför måste den virtuella datorn köra en version av operativ systemet Windows.

### Exempel 2: skapa en virtuell dator för Linux-operativsystemet genom att använda en mall
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

Det första kommandot skapar ett **PSCredential** -objekt och lagrar det sedan i $credentials variabel.

Det andra kommandot hämtar mallen för virtuell dator med namnet ContosoTemplate19 med hjälp av cmdleten **Get-WAPackVMTemplate** och lagrar den sedan i $Template variabel.

Med kommandot slut skapas en virtuell dator med namnet ContosoV028, baserat på mallen som lagras i $Template variabel.
Kommandot anger *Linux* -parametern och därför måste den virtuella datorn köra en version av Linux-operativsystemet.

### Exempel 3: skapa en virtuell dator från en hård disk och storleks profil
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

Det första kommandot får en operativ system disk som heter ContosoDiskOS med hjälp av cmdleten **Get-WAPackVMOSDisk** och lagrar den sedan i $OSDisk variabel.

Det andra kommandot får storleks profilen "MediumSizeVM" med cmdleten **Get-WAPackVMSizeProfile** och lagrar den sedan i $SizeProfile variabel.

Med kommandot slut skapas en virtuell dator med namnet ContosoV073 från operativ system disken som lagras i $OSDisk och den profil som lagras i $SizeProfile.

## MALLPARAMETRAR

### -AdministratorSSHKey
Anger SSH-tangenten (Secure Shell) för administratörs kontot.

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Anger att cmdleten skapar en virtuell dator som kör Linux-operativsystemet.

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -OSDisk
Anger en operativ system disk som ett **VirtualHardDisk** -objekt.
Använd cmdleten **Get-WAPackVMOSDisk** för att få en operativ system disk.

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductKey
Anger en produkt nyckeln.
Produkt nyckeln är ett 25-siffrigt nummer som identifierar produkt licensen.
Använd en produkt nyckeln för ett operativ system som du planerar att installera på en virtuell dator eller värd.

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
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
Använd cmdleten Get-WAPackVMTemplate för att hämta ett Template-objekt.

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
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
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSizeProfile
Anger en storleks profil för en virtuell dator som ett **HardwareProfile** -objekt.
Använd cmdleten **Get-WAPackVMSizeProfile** för att få en storleks profil.

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VNet
Anger ett virtuellt nätverk.
Cmdleten ansluter den virtuella datorn till det virtuella nätverk som du anger.
Använd cmdleten **Get-WAPackVNet** för att få ett virtuellt nätverk.

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Windows
Anger att cmdleten skapar en virtuell dator för att köra operativ systemet Windows.

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
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

[Get-WAPackVM](./Get-WAPackVM.md)

[Remove-WAPackVM](./Remove-WAPackVM.md)

[Restart-WAPackVM](./Restart-WAPackVM.md)

[Resume-WAPackVM](./Resume-WAPackVM.md)

[Set-WAPackVM](./Set-WAPackVM.md)

[Start-WAPackVM](./Start-WAPackVM.md)

[Stopp-WAPackVM](./Stop-WAPackVM.md)

[Suspend-WAPackVM](./Suspend-WAPackVM.md)

[Get-WAPackVMSizeProfile](./Get-WAPackVMSizeProfile.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)

[Get-WAPackVMOSDisk](./Get-WAPackVMOSDisk.md)


