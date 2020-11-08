---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0C806C0A-C199-4AF4-AE2A-11A2467A0873
online version: ''
schema: 2.0.0
ms.openlocfilehash: b11db019a3d7707ce93b2b2355efbaabe77fb91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099218"
---
# <span data-ttu-id="6aace-101">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="6aace-101">New-AzureSBNamespace</span></span>

## <span data-ttu-id="6aace-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6aace-102">SYNOPSIS</span></span>
<span data-ttu-id="6aace-103">Skapar ett namn område.</span><span class="sxs-lookup"><span data-stu-id="6aace-103">Creates a namespace.</span></span>

## <span data-ttu-id="6aace-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6aace-104">SYNTAX</span></span>

```
New-AzureSBNamespace -Name <String> [-Location <String>] [-CreateACSNamespace <Boolean>]
 -NamespaceType <NamespaceType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6aace-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6aace-105">DESCRIPTION</span></span>
<span data-ttu-id="6aace-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="6aace-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6aace-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6aace-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6aace-108">Cmdleten **New-AzureSBNamespace** skapar ett tjänst namn område som ska användas med Service Bus in Azure.</span><span class="sxs-lookup"><span data-stu-id="6aace-108">The **New-AzureSBNamespace** cmdlet creates a service namespace for use with Service Bus in Azure.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="6aace-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6aace-109">EXAMPLES</span></span>

### <span data-ttu-id="6aace-110">Exempel 1: skapa ett tjänst namn område</span><span class="sxs-lookup"><span data-stu-id="6aace-110">Example 1: Create a service namespace</span></span>
```
PS C:\> New-AzureSBNamespace -Name myNameSpace -Location East US 
PS C:\> New-AzureSBNamespace myNameSpace 'East US'
```

<span data-ttu-id="6aace-111">Exemplen skapar en tjänst namn rymd som ska användas med Service Bus in Azure.</span><span class="sxs-lookup"><span data-stu-id="6aace-111">The examples create a service namespace for use with Service Bus in Azure.</span></span>
<span data-ttu-id="6aace-112">Båda exemplen innehåller de obligatoriska parameter värdena, men endast den första inkluderar parameter namnen.</span><span class="sxs-lookup"><span data-stu-id="6aace-112">Both examples include the required parameter values, but only the first includes the parameter names.</span></span>
<span data-ttu-id="6aace-113">Det andra exemplet kan användas eftersom båda parametrarna är placerade och deras värden anges i den ordning som krävs.</span><span class="sxs-lookup"><span data-stu-id="6aace-113">The second example can be used because both parameters are positional and their values are given in the required order.</span></span>

## <span data-ttu-id="6aace-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6aace-114">PARAMETERS</span></span>

### <span data-ttu-id="6aace-115">-CreateACSNamespace</span><span class="sxs-lookup"><span data-stu-id="6aace-115">-CreateACSNamespace</span></span>
<span data-ttu-id="6aace-116">Anger om du vill skapa ett tillhör ande ACS-namnrymd utöver tjänst namn området.</span><span class="sxs-lookup"><span data-stu-id="6aace-116">Specifies whether to create an associated ACS namespace in addition to the service namespace.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aace-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="6aace-117">-Location</span></span>
<span data-ttu-id="6aace-118">Anger en region för det nya namn området.</span><span class="sxs-lookup"><span data-stu-id="6aace-118">Specifies a region for the new namespace.</span></span>

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

### <span data-ttu-id="6aace-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="6aace-119">-Name</span></span>
<span data-ttu-id="6aace-120">Anger ett namn för det nya namn området.</span><span class="sxs-lookup"><span data-stu-id="6aace-120">Specifies a name for the new namespace.</span></span>

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

### <span data-ttu-id="6aace-121">-NamespaceType</span><span class="sxs-lookup"><span data-stu-id="6aace-121">-NamespaceType</span></span>
<span data-ttu-id="6aace-122">Ange om namn området ska användas för meddelande-och aviserings nav.</span><span class="sxs-lookup"><span data-stu-id="6aace-122">Specify a whether to use the namespace for Messaging or Notification Hubs.</span></span>

```yaml
Type: NamespaceType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aace-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="6aace-123">-Profile</span></span>
<span data-ttu-id="6aace-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6aace-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6aace-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6aace-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6aace-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aace-126">CommonParameters</span></span>
<span data-ttu-id="6aace-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aace-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aace-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aace-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aace-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6aace-129">INPUTS</span></span>

## <span data-ttu-id="6aace-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6aace-130">OUTPUTS</span></span>

## <span data-ttu-id="6aace-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6aace-131">NOTES</span></span>

## <span data-ttu-id="6aace-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6aace-132">RELATED LINKS</span></span>

[<span data-ttu-id="6aace-133">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="6aace-133">Remove-AzureSBNamespace</span></span>](./Remove-AzureSBNamespace.md)


