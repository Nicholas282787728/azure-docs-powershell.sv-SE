---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: d7f52ded01ce5b785c1e935ba8d3ebf4b1c0a5fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404952"
---
# <span data-ttu-id="055f0-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="055f0-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="055f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="055f0-102">SYNOPSIS</span></span>
<span data-ttu-id="055f0-103">Uppdaterar en virtuell router.</span><span class="sxs-lookup"><span data-stu-id="055f0-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="055f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="055f0-104">SYNTAX</span></span>

### <span data-ttu-id="055f0-105">VirtualRouterNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="055f0-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="055f0-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="055f0-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="055f0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="055f0-107">DESCRIPTION</span></span>
<span data-ttu-id="055f0-108">Uppdaterar virtuell router för att aktivera eller inaktivera gren till gren trafik.</span><span class="sxs-lookup"><span data-stu-id="055f0-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="055f0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="055f0-109">EXAMPLES</span></span>

### <span data-ttu-id="055f0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="055f0-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="055f0-111">Uppdaterar den virtuella routern för att tillåta filial till gren trafik</span><span class="sxs-lookup"><span data-stu-id="055f0-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="055f0-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="055f0-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="055f0-113">Uppdaterar den virtuella routern för att blockera gren till gren trafik</span><span class="sxs-lookup"><span data-stu-id="055f0-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="055f0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="055f0-114">PARAMETERS</span></span>

### <span data-ttu-id="055f0-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="055f0-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="055f0-116">Flagga för att tillåta filial till gren trafik för virtuell router.</span><span class="sxs-lookup"><span data-stu-id="055f0-116">Flag to allow branch to branch traffic for virtual router.</span></span>

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

### <span data-ttu-id="055f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="055f0-117">-DefaultProfile</span></span>
<span data-ttu-id="055f0-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="055f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="055f0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="055f0-119">-ResourceGroupName</span></span>
<span data-ttu-id="055f0-120">Namnet på den virtuella routern i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="055f0-120">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055f0-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="055f0-121">-ResourceId</span></span>
<span data-ttu-id="055f0-122">ResourceId för den virtuella routern.</span><span class="sxs-lookup"><span data-stu-id="055f0-122">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055f0-123">-RouterName</span><span class="sxs-lookup"><span data-stu-id="055f0-123">-RouterName</span></span>
<span data-ttu-id="055f0-124">Namnet på den virtuella routern.</span><span class="sxs-lookup"><span data-stu-id="055f0-124">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055f0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="055f0-125">CommonParameters</span></span>
<span data-ttu-id="055f0-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="055f0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="055f0-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="055f0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="055f0-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="055f0-128">INPUTS</span></span>

### <span data-ttu-id="055f0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="055f0-129">System.String</span></span>

## <span data-ttu-id="055f0-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="055f0-130">OUTPUTS</span></span>

### <span data-ttu-id="055f0-131">Microsoft. Azure. commands. Networks. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="055f0-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="055f0-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="055f0-132">NOTES</span></span>

## <span data-ttu-id="055f0-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="055f0-133">RELATED LINKS</span></span>
