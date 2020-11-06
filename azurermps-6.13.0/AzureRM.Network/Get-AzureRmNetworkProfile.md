---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
ms.openlocfilehash: 5bdd5e5d5212564afb1f9b06f220e8c452bcbbaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586336"
---
# <span data-ttu-id="ecee7-101">Get-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ecee7-101">Get-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="ecee7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecee7-102">SYNOPSIS</span></span>
<span data-ttu-id="ecee7-103">Hämtar en befintlig nätverks profil på toppnivå resursen</span><span class="sxs-lookup"><span data-stu-id="ecee7-103">Gets an existing network profile top level resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecee7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecee7-104">SYNTAX</span></span>

### <span data-ttu-id="ecee7-105">Noexpandering (standard)</span><span class="sxs-lookup"><span data-stu-id="ecee7-105">NoExpand (Default)</span></span>
```
Get-AzureRmNetworkProfile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecee7-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecee7-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecee7-107">GetByResourceNameNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecee7-107">GetByResourceNameNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile [-ResourceGroupName <String>] [-Name <String>] -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecee7-108">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecee7-108">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecee7-109">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecee7-109">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecee7-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecee7-110">DESCRIPTION</span></span>
<span data-ttu-id="ecee7-111">Cmdleten **Get-AzureRmNetworkProfile** hämtar en befintlig nätverks profil på toppnivå resursen</span><span class="sxs-lookup"><span data-stu-id="ecee7-111">The **Get-AzureRmNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="ecee7-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecee7-112">EXAMPLES</span></span>

### <span data-ttu-id="ecee7-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ecee7-113">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="ecee7-114">Då hämtas nätverks profil NP1 i resurs gruppen RG1</span><span class="sxs-lookup"><span data-stu-id="ecee7-114">This retrieves the network profile np1 in resource group rg1</span></span>

## <span data-ttu-id="ecee7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecee7-115">PARAMETERS</span></span>

### <span data-ttu-id="ecee7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecee7-116">-DefaultProfile</span></span>
<span data-ttu-id="ecee7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ecee7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecee7-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ecee7-118">-ExpandResource</span></span>
<span data-ttu-id="ecee7-119">Resurs referensen som ska expanderas.</span><span class="sxs-lookup"><span data-stu-id="ecee7-119">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceNameNoExpandParameterSet, GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecee7-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ecee7-120">-Name</span></span>
<span data-ttu-id="ecee7-121">Namnet på nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="ecee7-121">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecee7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecee7-122">-ResourceGroupName</span></span>
<span data-ttu-id="ecee7-123">Namnet på resurs gruppen för nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="ecee7-123">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecee7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecee7-124">-ResourceId</span></span>
<span data-ttu-id="ecee7-125">Azure Resource Manager-ID för nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="ecee7-125">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecee7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecee7-126">CommonParameters</span></span>
<span data-ttu-id="ecee7-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecee7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecee7-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecee7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecee7-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecee7-129">INPUTS</span></span>

### <span data-ttu-id="ecee7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ecee7-130">System.String</span></span>

## <span data-ttu-id="ecee7-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecee7-131">OUTPUTS</span></span>

### <span data-ttu-id="ecee7-132">Microsoft. Azure. commands. Networks. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ecee7-132">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="ecee7-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecee7-133">NOTES</span></span>

## <span data-ttu-id="ecee7-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecee7-134">RELATED LINKS</span></span>
