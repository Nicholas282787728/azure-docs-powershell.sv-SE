---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: 1fbe9e790966a92c38ba79b56221e5e6083b649c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525688"
---
# <span data-ttu-id="9ff7e-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="9ff7e-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="9ff7e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ff7e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff7e-103">Hämtar säkerhetslösningar som upptäckts av Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="9ff7e-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="9ff7e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ff7e-104">SYNTAX</span></span>

### <span data-ttu-id="9ff7e-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="9ff7e-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ff7e-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="9ff7e-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ff7e-107">ID</span><span class="sxs-lookup"><span data-stu-id="9ff7e-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ff7e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ff7e-108">DESCRIPTION</span></span>
<span data-ttu-id="9ff7e-109">Säkerhetslösningar identifieras automatiskt av Azure Security Center, Använd denna cmdlet för att Visa upptäckta säkerhetslösningar</span><span class="sxs-lookup"><span data-stu-id="9ff7e-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="9ff7e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ff7e-110">EXAMPLES</span></span>

### <span data-ttu-id="9ff7e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9ff7e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="9ff7e-112">Få alla upptäckta säkerhetslösningar i abonnemanget</span><span class="sxs-lookup"><span data-stu-id="9ff7e-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="9ff7e-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9ff7e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="9ff7e-114">Skaffa en specifik upptäckd säkerhets lösning</span><span class="sxs-lookup"><span data-stu-id="9ff7e-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="9ff7e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ff7e-115">PARAMETERS</span></span>

### <span data-ttu-id="9ff7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff7e-116">-DefaultProfile</span></span>
<span data-ttu-id="9ff7e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9ff7e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff7e-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="9ff7e-118">-Location</span></span>
<span data-ttu-id="9ff7e-119">Plats.</span><span class="sxs-lookup"><span data-stu-id="9ff7e-119">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff7e-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9ff7e-120">-Name</span></span>
<span data-ttu-id="9ff7e-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="9ff7e-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff7e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ff7e-122">-ResourceGroupName</span></span>
<span data-ttu-id="9ff7e-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="9ff7e-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff7e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ff7e-124">-ResourceId</span></span>
<span data-ttu-id="9ff7e-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9ff7e-125">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff7e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff7e-126">CommonParameters</span></span>
<span data-ttu-id="9ff7e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff7e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff7e-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ff7e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff7e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ff7e-129">INPUTS</span></span>

### <span data-ttu-id="9ff7e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9ff7e-130">System.String</span></span>

## <span data-ttu-id="9ff7e-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ff7e-131">OUTPUTS</span></span>

### <span data-ttu-id="9ff7e-132">Microsoft. Azure. commands. Security. Models. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="9ff7e-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="9ff7e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ff7e-133">NOTES</span></span>

## <span data-ttu-id="9ff7e-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ff7e-134">RELATED LINKS</span></span>
