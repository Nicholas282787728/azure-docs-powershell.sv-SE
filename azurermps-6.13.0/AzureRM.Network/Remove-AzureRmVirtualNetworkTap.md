---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 59e3b7f233077c8ed7064bcb1757634fe08c262b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576163"
---
# <span data-ttu-id="abda1-101">Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="abda1-101">Remove-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="abda1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abda1-102">SYNOPSIS</span></span>
<span data-ttu-id="abda1-103">Tar bort ett virtuellt nätverk tryck.</span><span class="sxs-lookup"><span data-stu-id="abda1-103">Removes a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abda1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abda1-104">SYNTAX</span></span>

### <span data-ttu-id="abda1-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="abda1-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abda1-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abda1-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abda1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abda1-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abda1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abda1-108">DESCRIPTION</span></span>
<span data-ttu-id="abda1-109">Cmdleten **Remove-AzureRmVirtualNetworkTap** tar bort ett Azure Virtual Network-tryck.</span><span class="sxs-lookup"><span data-stu-id="abda1-109">The **Remove-AzureRmVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="abda1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abda1-110">EXAMPLES</span></span>

### <span data-ttu-id="abda1-111">Exempel 1: ta bort ett virtuak nätverk tryck</span><span class="sxs-lookup"><span data-stu-id="abda1-111">Example 1: Remove a virtuak network tap</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="abda1-112">Det här kommandot tar bort VirtualNetworkTap1 i ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="abda1-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="abda1-113">Eftersom *Force* -parametern inte används uppmanas användaren att bekräfta åtgärden.</span><span class="sxs-lookup"><span data-stu-id="abda1-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="abda1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abda1-114">PARAMETERS</span></span>

### <span data-ttu-id="abda1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="abda1-115">-AsJob</span></span>
<span data-ttu-id="abda1-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="abda1-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abda1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abda1-117">-DefaultProfile</span></span>
<span data-ttu-id="abda1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="abda1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abda1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="abda1-119">-Force</span></span>
<span data-ttu-id="abda1-120">Fråga inte efter bekräftelse om du vill ta bort resursen</span><span class="sxs-lookup"><span data-stu-id="abda1-120">Do not ask for confirmation if you want to delete resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abda1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abda1-121">-InputObject</span></span>
<span data-ttu-id="abda1-122">Referens till VirtualNetworkTap-resursen</span><span class="sxs-lookup"><span data-stu-id="abda1-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abda1-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="abda1-123">-Name</span></span>
<span data-ttu-id="abda1-124">Namnet på tryckningen.</span><span class="sxs-lookup"><span data-stu-id="abda1-124">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abda1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abda1-125">-PassThru</span></span>
<span data-ttu-id="abda1-126">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="abda1-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="abda1-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="abda1-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abda1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abda1-128">-ResourceGroupName</span></span>
<span data-ttu-id="abda1-129">Resurs grupps namnet för det virtuella nätverkets tryck.</span><span class="sxs-lookup"><span data-stu-id="abda1-129">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abda1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abda1-130">-ResourceId</span></span>
<span data-ttu-id="abda1-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="abda1-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abda1-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="abda1-132">-Confirm</span></span>
<span data-ttu-id="abda1-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="abda1-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abda1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abda1-134">-WhatIf</span></span>
<span data-ttu-id="abda1-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="abda1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abda1-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="abda1-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abda1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abda1-137">CommonParameters</span></span>
<span data-ttu-id="abda1-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abda1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abda1-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abda1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abda1-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abda1-140">INPUTS</span></span>

### <span data-ttu-id="abda1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="abda1-141">System.String</span></span>

## <span data-ttu-id="abda1-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abda1-142">OUTPUTS</span></span>

### <span data-ttu-id="abda1-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="abda1-143">System.Boolean</span></span>

## <span data-ttu-id="abda1-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abda1-144">NOTES</span></span>

## <span data-ttu-id="abda1-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abda1-145">RELATED LINKS</span></span>
