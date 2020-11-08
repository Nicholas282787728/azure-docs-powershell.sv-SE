---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: B83ABF05-3169-4D05-AB6E-167DE045595D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fea9341b288b5c2f98413cc95cb42bffe1a78ca3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093189"
---
# <span data-ttu-id="af753-101">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="af753-101">Restore-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="af753-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af753-102">SYNOPSIS</span></span>
<span data-ttu-id="af753-103">Distribuerar en tidigare distribution av en webbplats i Azure.</span><span class="sxs-lookup"><span data-stu-id="af753-103">Redeploys a previous deployment of a website in Azure.</span></span>

## <span data-ttu-id="af753-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af753-104">SYNTAX</span></span>

```
Restore-AzureWebsiteDeployment [-CommitId <String>] [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af753-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af753-105">DESCRIPTION</span></span>
<span data-ttu-id="af753-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="af753-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="af753-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="af753-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="af753-108">Cmdleten **restore-AzureWebsiteDeployment** återdistribuerar en tidigare distribution av en webbplats i Azure.</span><span class="sxs-lookup"><span data-stu-id="af753-108">The **Restore-AzureWebsiteDeployment** cmdlet redeploys a previous deployment of a website in Azure.</span></span>
<span data-ttu-id="af753-109">Den här processen ersätter den nuvarande distributionen med den valda distributionen.</span><span class="sxs-lookup"><span data-stu-id="af753-109">This process replaces the current deployment with the selected deployment.</span></span>

## <span data-ttu-id="af753-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af753-110">EXAMPLES</span></span>

### <span data-ttu-id="af753-111">Exempel 1: Distribuera om en webbplats</span><span class="sxs-lookup"><span data-stu-id="af753-111">Example 1: Redeploy a site</span></span>
```
PS C:\> Restore-AzureWebsiteDeployment -Name "ContosoSite" -CommitId "f876543210"
```

<span data-ttu-id="af753-112">Det här kommandot distribuerar om distributionen med ID-f876543210 för webbplatsen ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="af753-112">This command redeploys the deployment that has the ID f876543210 for the website named ContosoSite.</span></span>

## <span data-ttu-id="af753-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af753-113">PARAMETERS</span></span>

### <span data-ttu-id="af753-114">-CommitId</span><span class="sxs-lookup"><span data-stu-id="af753-114">-CommitId</span></span>
<span data-ttu-id="af753-115">Anger identifieringen för distributionen som ska omdistribueras.</span><span class="sxs-lookup"><span data-stu-id="af753-115">Specifies the identifier of the deployment to redeploy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af753-116">-Force</span><span class="sxs-lookup"><span data-stu-id="af753-116">-Force</span></span>
<span data-ttu-id="af753-117">Om den här funktionen är aktive rad distribueras den tidigare distributionen utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="af753-117">If enabled, redeploys the previous deployment without prompting for confirmation.</span></span>

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

### <span data-ttu-id="af753-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="af753-118">-Name</span></span>
<span data-ttu-id="af753-119">Anger namnet på den webbplats som ska omdistribueras.</span><span class="sxs-lookup"><span data-stu-id="af753-119">Specifies the name of the website to redeploy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af753-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="af753-120">-Profile</span></span>
<span data-ttu-id="af753-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="af753-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="af753-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="af753-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="af753-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="af753-123">-Slot</span></span>
<span data-ttu-id="af753-124">Anger plats namnet.</span><span class="sxs-lookup"><span data-stu-id="af753-124">Specifies the slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af753-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af753-125">-Confirm</span></span>
<span data-ttu-id="af753-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af753-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af753-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af753-127">-WhatIf</span></span>
<span data-ttu-id="af753-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af753-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af753-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af753-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af753-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af753-130">CommonParameters</span></span>
<span data-ttu-id="af753-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af753-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af753-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af753-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af753-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af753-133">INPUTS</span></span>

## <span data-ttu-id="af753-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af753-134">OUTPUTS</span></span>

## <span data-ttu-id="af753-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af753-135">NOTES</span></span>

## <span data-ttu-id="af753-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af753-136">RELATED LINKS</span></span>

[<span data-ttu-id="af753-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="af753-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="af753-138">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="af753-138">Get-AzureWebsiteDeployment</span></span>](./Get-AzureWebsiteDeployment.md)


