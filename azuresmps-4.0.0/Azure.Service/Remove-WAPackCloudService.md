---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1ECF6BB5-3751-4DA0-AC6C-A64F15F46D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552c2511a806abb4329860e7c15d8a68b5e03f79
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100643"
---
# <span data-ttu-id="da758-101">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="da758-101">Remove-WAPackCloudService</span></span>

## <span data-ttu-id="da758-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da758-102">SYNOPSIS</span></span>
<span data-ttu-id="da758-103">Tar bort moln tjänst objekt.</span><span class="sxs-lookup"><span data-stu-id="da758-103">Removes cloud service objects.</span></span>

## <span data-ttu-id="da758-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da758-104">SYNTAX</span></span>

```
Remove-WAPackCloudService -CloudService <CloudService> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da758-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da758-105">DESCRIPTION</span></span>
<span data-ttu-id="da758-106">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="da758-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="da758-107">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="da758-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="da758-108">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="da758-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="da758-109">Cmdleten **Remove-WAPackCloudService** tar bort moln tjänst objekt.</span><span class="sxs-lookup"><span data-stu-id="da758-109">The **Remove-WAPackCloudService** cmdlet removes cloud service objects.</span></span>

## <span data-ttu-id="da758-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da758-110">EXAMPLES</span></span>

### <span data-ttu-id="da758-111">Exempel 1: ta bort en moln tjänst</span><span class="sxs-lookup"><span data-stu-id="da758-111">Example 1: Remove a cloud service</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService01"
PS C:\> Remove-WAPackVM -VM $CloudService
```

<span data-ttu-id="da758-112">Det första kommandot får moln tjänsten med namnet ContosoCloudService01 med hjälp av cmdleten **Get-WAPackCloudService** och lagrar sedan objektet i variabeln $CloudService.</span><span class="sxs-lookup"><span data-stu-id="da758-112">The first command gets the cloud service named ContosoCloudService01 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="da758-113">Det andra kommandot tar bort den cloudservice som är lagrad i $CloudService.</span><span class="sxs-lookup"><span data-stu-id="da758-113">The second command removes the cloudservice stored in $CloudService.</span></span>
<span data-ttu-id="da758-114">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="da758-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="da758-115">Exempel 2: ta bort en moln tjänst utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="da758-115">Example 2: Remove a cloud service without confirmation</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService02"
PS C:\> Remove-WAPackCloudService -VM $CloudService -Force
```

<span data-ttu-id="da758-116">Det första kommandot får moln tjänsten med namnet ContosoCloudService02 med hjälp av cmdleten **Get-WAPackCloudService** och lagrar sedan objektet i variabeln $CloudService.</span><span class="sxs-lookup"><span data-stu-id="da758-116">The first command gets the cloud service named ContosoCloudService02 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="da758-117">Det andra kommandot tar bort moln tjänsten som är lagrad i $CloudService.</span><span class="sxs-lookup"><span data-stu-id="da758-117">The second command removes the cloud service stored in $CloudService.</span></span>
<span data-ttu-id="da758-118">Det här kommandot innehåller parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="da758-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="da758-119">Du uppmanas inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="da758-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="da758-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da758-120">PARAMETERS</span></span>

### <span data-ttu-id="da758-121">-CloudService</span><span class="sxs-lookup"><span data-stu-id="da758-121">-CloudService</span></span>
<span data-ttu-id="da758-122">Anger ett moln tjänst objekt.</span><span class="sxs-lookup"><span data-stu-id="da758-122">Specifies a cloud service object.</span></span>
<span data-ttu-id="da758-123">Använd cmdleten **Get-WAPackCloudService** för att få en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="da758-123">To obtain a cloud service, use the **Get-WAPackCloudService** cmdlet.</span></span>

```yaml
Type: CloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da758-124">-Force</span><span class="sxs-lookup"><span data-stu-id="da758-124">-Force</span></span>
<span data-ttu-id="da758-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="da758-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da758-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da758-126">-PassThru</span></span>
<span data-ttu-id="da758-127">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="da758-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="da758-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="da758-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="da758-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="da758-129">-Profile</span></span>
<span data-ttu-id="da758-130">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="da758-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="da758-131">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="da758-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da758-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da758-132">-Confirm</span></span>
<span data-ttu-id="da758-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da758-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da758-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da758-134">-WhatIf</span></span>
<span data-ttu-id="da758-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da758-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da758-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da758-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da758-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da758-137">CommonParameters</span></span>
<span data-ttu-id="da758-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da758-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da758-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da758-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da758-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da758-140">INPUTS</span></span>

## <span data-ttu-id="da758-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da758-141">OUTPUTS</span></span>

## <span data-ttu-id="da758-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da758-142">NOTES</span></span>

## <span data-ttu-id="da758-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da758-143">RELATED LINKS</span></span>

[<span data-ttu-id="da758-144">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="da758-144">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="da758-145">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="da758-145">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)


