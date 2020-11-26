---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2497b41399c79297726bc82e3232934cbd6768d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103175"
---
# <span data-ttu-id="bba21-101">Get-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="bba21-101">Get-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="bba21-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bba21-102">SYNOPSIS</span></span>
<span data-ttu-id="bba21-103">Konto för att få avstånd till ankare</span><span class="sxs-lookup"><span data-stu-id="bba21-103">Get Spatial Anchors Account</span></span>

## <span data-ttu-id="bba21-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bba21-104">SYNTAX</span></span>

### <span data-ttu-id="bba21-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bba21-105">ListParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bba21-106">GetParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bba21-106">GetParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bba21-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bba21-107">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bba21-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bba21-108">DESCRIPTION</span></span>
<span data-ttu-id="bba21-109">Få eller Visa en lista över spatiala ankare i vissa abonnemang och resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="bba21-109">Get or list Spatial Anchors Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="bba21-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bba21-110">EXAMPLES</span></span>

### <span data-ttu-id="bba21-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bba21-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : 2f7443d0-2c2b-4514-9b29-a78072a1556f
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/2f7443d0-2c2b-4514-9b29-a78072a1556f/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/demo
Name                : demo
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : ed3273ce-1eeb-42c7-b3b8-fb9896b9801c
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/ed3273ce-1eeb-42c7-b3b8-fb9896b9801c/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/foobar
Name                : foobar
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="bba21-112">Visa alla spatialdata för ankare i resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="bba21-112">List all Spatial Anchors Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="bba21-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bba21-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mrc-anchor-prod.trafficmanager.net
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="bba21-114">Kontot för spatiala ankare "exempel" i resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="bba21-114">Get Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="bba21-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bba21-115">PARAMETERS</span></span>

### <span data-ttu-id="bba21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba21-116">-DefaultProfile</span></span>
<span data-ttu-id="bba21-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bba21-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba21-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="bba21-118">-Name</span></span>
<span data-ttu-id="bba21-119">Konto namn för spatialdata.</span><span class="sxs-lookup"><span data-stu-id="bba21-119">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba21-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba21-120">-ResourceGroupName</span></span>
<span data-ttu-id="bba21-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="bba21-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba21-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bba21-122">-ResourceId</span></span>
<span data-ttu-id="bba21-123">Resurs-ID för konton med Spatial ankare.</span><span class="sxs-lookup"><span data-stu-id="bba21-123">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba21-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba21-124">CommonParameters</span></span>
<span data-ttu-id="bba21-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bba21-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bba21-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bba21-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba21-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bba21-127">INPUTS</span></span>

### <span data-ttu-id="bba21-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bba21-128">System.String</span></span>

## <span data-ttu-id="bba21-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bba21-129">OUTPUTS</span></span>

### <span data-ttu-id="bba21-130">Microsoft. Azure. commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="bba21-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="bba21-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bba21-131">NOTES</span></span>

## <span data-ttu-id="bba21-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bba21-132">RELATED LINKS</span></span>