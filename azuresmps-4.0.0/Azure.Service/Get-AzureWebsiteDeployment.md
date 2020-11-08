---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D15329E9-BB72-4F1B-B79A-E7AD920A9D5A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c972bb693a1e13b365635064785182c53af409
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099739"
---
# <span data-ttu-id="78fb6-101">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="78fb6-101">Get-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="78fb6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="78fb6-103">Hämtar distributionerna för en webbplats.</span><span class="sxs-lookup"><span data-stu-id="78fb6-103">Gets the deployments for a website.</span></span>

## <span data-ttu-id="78fb6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78fb6-104">SYNTAX</span></span>

```
Get-AzureWebsiteDeployment [-CommitId <String>] [-MaxResults <Int32>] [-Details] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="78fb6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78fb6-105">DESCRIPTION</span></span>
<span data-ttu-id="78fb6-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="78fb6-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="78fb6-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="78fb6-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="78fb6-108">Hämtar distributionerna för en webbplats i Azure.</span><span class="sxs-lookup"><span data-stu-id="78fb6-108">Gets the deployments for a website in Azure.</span></span>

## <span data-ttu-id="78fb6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78fb6-109">EXAMPLES</span></span>

## <span data-ttu-id="78fb6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78fb6-110">PARAMETERS</span></span>

### <span data-ttu-id="78fb6-111">-CommitId</span><span class="sxs-lookup"><span data-stu-id="78fb6-111">-CommitId</span></span>
<span data-ttu-id="78fb6-112">Anger distributionens unika ID.</span><span class="sxs-lookup"><span data-stu-id="78fb6-112">Specifies the unique ID for the deployment.</span></span>

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

### <span data-ttu-id="78fb6-113">-Detaljer</span><span class="sxs-lookup"><span data-stu-id="78fb6-113">-Details</span></span>
<span data-ttu-id="78fb6-114">Visar detaljerad information om distributionerna.</span><span class="sxs-lookup"><span data-stu-id="78fb6-114">Shows detailed information about the deployments.</span></span>

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

### <span data-ttu-id="78fb6-115">-MaxResults</span><span class="sxs-lookup"><span data-stu-id="78fb6-115">-MaxResults</span></span>
<span data-ttu-id="78fb6-116">Anger det största antal resultat som ska returneras av kommandot.</span><span class="sxs-lookup"><span data-stu-id="78fb6-116">Specifies the largest number of results that you want the command to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78fb6-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="78fb6-117">-Name</span></span>
<span data-ttu-id="78fb6-118">Anger namnet på den webbplats där du vill få distributions information.</span><span class="sxs-lookup"><span data-stu-id="78fb6-118">Specifies the name of the website for which you want to get deployment information.</span></span>

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

### <span data-ttu-id="78fb6-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="78fb6-119">-Profile</span></span>
<span data-ttu-id="78fb6-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="78fb6-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="78fb6-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="78fb6-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="78fb6-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="78fb6-122">-Slot</span></span>
<span data-ttu-id="78fb6-123">Anger plats namnet.</span><span class="sxs-lookup"><span data-stu-id="78fb6-123">Specifies the slot name.</span></span>

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

### <span data-ttu-id="78fb6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78fb6-124">CommonParameters</span></span>
<span data-ttu-id="78fb6-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78fb6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78fb6-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78fb6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78fb6-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78fb6-127">INPUTS</span></span>

## <span data-ttu-id="78fb6-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78fb6-128">OUTPUTS</span></span>

## <span data-ttu-id="78fb6-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78fb6-129">NOTES</span></span>

## <span data-ttu-id="78fb6-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78fb6-130">RELATED LINKS</span></span>

[<span data-ttu-id="78fb6-131">Återställ-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="78fb6-131">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


