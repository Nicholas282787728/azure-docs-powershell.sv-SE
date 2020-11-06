---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
ms.openlocfilehash: ecea7ba6aa34df73de65a4d03e004531e81ff497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576086"
---
# <span data-ttu-id="67f85-101">Get-AzureRmDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="67f85-101">Get-AzureRmDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="67f85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67f85-102">SYNOPSIS</span></span>
<span data-ttu-id="67f85-103">Hämtar säkerhetslösningar som upptäckts av Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="67f85-103">Gets security solutions that were discovered by Azure Security Center</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67f85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67f85-104">SYNTAX</span></span>

### <span data-ttu-id="67f85-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="67f85-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67f85-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="67f85-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67f85-107">ID</span><span class="sxs-lookup"><span data-stu-id="67f85-107">ResourceId</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67f85-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67f85-108">DESCRIPTION</span></span>
<span data-ttu-id="67f85-109">Säkerhetslösningar identifieras automatiskt av Azure Security Center, Använd denna cmdlet för att Visa upptäckta säkerhetslösningar</span><span class="sxs-lookup"><span data-stu-id="67f85-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="67f85-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67f85-110">EXAMPLES</span></span>

### <span data-ttu-id="67f85-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="67f85-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="67f85-112">Få alla upptäckta säkerhetslösningar i abonnemanget</span><span class="sxs-lookup"><span data-stu-id="67f85-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="67f85-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="67f85-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="67f85-114">Skaffa en specifik upptäckd säkerhets lösning</span><span class="sxs-lookup"><span data-stu-id="67f85-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="67f85-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67f85-115">PARAMETERS</span></span>

### <span data-ttu-id="67f85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f85-116">-DefaultProfile</span></span>
<span data-ttu-id="67f85-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67f85-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67f85-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="67f85-118">-Location</span></span>
<span data-ttu-id="67f85-119">Plats.</span><span class="sxs-lookup"><span data-stu-id="67f85-119">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67f85-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="67f85-120">-Name</span></span>
<span data-ttu-id="67f85-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="67f85-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67f85-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67f85-122">-ResourceGroupName</span></span>
<span data-ttu-id="67f85-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="67f85-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67f85-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67f85-124">-ResourceId</span></span>
<span data-ttu-id="67f85-125">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="67f85-125">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67f85-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f85-126">CommonParameters</span></span>
<span data-ttu-id="67f85-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67f85-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f85-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67f85-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f85-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67f85-129">INPUTS</span></span>

### <span data-ttu-id="67f85-130">System. String</span><span class="sxs-lookup"><span data-stu-id="67f85-130">System.String</span></span>

## <span data-ttu-id="67f85-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67f85-131">OUTPUTS</span></span>

### <span data-ttu-id="67f85-132">Microsoft. Azure. commands. Security. Models. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="67f85-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="67f85-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67f85-133">NOTES</span></span>

## <span data-ttu-id="67f85-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67f85-134">RELATED LINKS</span></span>
