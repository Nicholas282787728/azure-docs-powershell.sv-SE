---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAB5E55D-95FC-4545-8BA6-EEFCFDB04200
online version: ''
schema: 2.0.0
ms.openlocfilehash: c311653b92219eb3bee0e3b1f8c8fe5caaee9846
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093363"
---
# <span data-ttu-id="e7814-101">Get-AzureOSVersion</span><span class="sxs-lookup"><span data-stu-id="e7814-101">Get-AzureOSVersion</span></span>

## <span data-ttu-id="e7814-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7814-102">SYNOPSIS</span></span>
<span data-ttu-id="e7814-103">Visar alla Azure gäst operativ system.</span><span class="sxs-lookup"><span data-stu-id="e7814-103">Lists all Azure guest operating systems.</span></span>

## <span data-ttu-id="e7814-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7814-104">SYNTAX</span></span>

```
Get-AzureOSVersion [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e7814-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7814-105">DESCRIPTION</span></span>
<span data-ttu-id="e7814-106">Cmdleten **Get-AzureOSVersion** visar alla tillgängliga Azure gäst operativ system.</span><span class="sxs-lookup"><span data-stu-id="e7814-106">The **Get-AzureOSVersion** cmdlet lists all the available Azure guest operating systems.</span></span>

## <span data-ttu-id="e7814-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7814-107">EXAMPLES</span></span>

### <span data-ttu-id="e7814-108">Exempel 1: Hämta alla tillgängliga operativ system</span><span class="sxs-lookup"><span data-stu-id="e7814-108">Example 1: Get all available operating systems</span></span>
```
PS C:\> Get-AzureOSVersion
```

<span data-ttu-id="e7814-109">Det här kommandot hämtar ett objekt som innehåller en lista över alla versioner av gäst operativ system som är tillgängliga i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e7814-109">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>

### <span data-ttu-id="e7814-110">Exempel 2: Visa information om operativ systemet i en tabell</span><span class="sxs-lookup"><span data-stu-id="e7814-110">Example 2: Display operating system information in a table</span></span>
```
PS C:\> Get-AzureOSVersion | Format-Table -AutoSize -Property "Family", "FamilyLabel", "Version"
```

<span data-ttu-id="e7814-111">Det här kommandot hämtar ett objekt som innehåller en lista över alla versioner av gäst operativ system som är tillgängliga i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e7814-111">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>
<span data-ttu-id="e7814-112">Kommandot skickar dem till **Format-Table-** cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="e7814-112">The command passes them to the **Format-Table** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e7814-113">Denna cmdlet formaterar dem som en tabell som visar operativ system familjen, operativ systemets familje etikett och version.</span><span class="sxs-lookup"><span data-stu-id="e7814-113">That cmdlet formats them as a table that shows the operating system family, operating system family label, and version.</span></span>

## <span data-ttu-id="e7814-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7814-114">PARAMETERS</span></span>

### <span data-ttu-id="e7814-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e7814-115">-InformationAction</span></span>
<span data-ttu-id="e7814-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="e7814-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e7814-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e7814-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7814-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="e7814-118">Continue</span></span>
- <span data-ttu-id="e7814-119">Över</span><span class="sxs-lookup"><span data-stu-id="e7814-119">Ignore</span></span>
- <span data-ttu-id="e7814-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="e7814-120">Inquire</span></span>
- <span data-ttu-id="e7814-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e7814-121">SilentlyContinue</span></span>
- <span data-ttu-id="e7814-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="e7814-122">Stop</span></span>
- <span data-ttu-id="e7814-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="e7814-123">Suspend</span></span>

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

### <span data-ttu-id="e7814-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e7814-124">-InformationVariable</span></span>
<span data-ttu-id="e7814-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="e7814-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e7814-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="e7814-126">-Profile</span></span>
<span data-ttu-id="e7814-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e7814-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7814-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e7814-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e7814-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7814-129">CommonParameters</span></span>
<span data-ttu-id="e7814-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7814-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7814-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7814-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7814-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7814-132">INPUTS</span></span>

## <span data-ttu-id="e7814-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7814-133">OUTPUTS</span></span>

## <span data-ttu-id="e7814-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7814-134">NOTES</span></span>

## <span data-ttu-id="e7814-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7814-135">RELATED LINKS</span></span>

[<span data-ttu-id="e7814-136">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="e7814-136">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)


