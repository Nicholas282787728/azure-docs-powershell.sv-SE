---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: bfe1c586d85a44460b1adbb84942be9b556973dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527592"
---
# <span data-ttu-id="2e948-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2e948-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="2e948-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e948-102">SYNOPSIS</span></span>
<span data-ttu-id="2e948-103">Tar bort ett virtuellt nätverk tryck.</span><span class="sxs-lookup"><span data-stu-id="2e948-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="2e948-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e948-104">SYNTAX</span></span>

### <span data-ttu-id="2e948-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2e948-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e948-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e948-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e948-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e948-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e948-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e948-108">DESCRIPTION</span></span>
<span data-ttu-id="2e948-109">Cmdleten **Remove-AzVirtualNetworkTap** tar bort ett Azure Virtual Network-tryck.</span><span class="sxs-lookup"><span data-stu-id="2e948-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="2e948-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e948-110">EXAMPLES</span></span>

### <span data-ttu-id="2e948-111">Exempel 1: ta bort ett virtuellt nätverk tryck</span><span class="sxs-lookup"><span data-stu-id="2e948-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="2e948-112">Det här kommandot tar bort VirtualNetworkTap1 i ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="2e948-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="2e948-113">Eftersom *Force* -parametern inte används uppmanas användaren att bekräfta åtgärden.</span><span class="sxs-lookup"><span data-stu-id="2e948-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="2e948-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e948-114">PARAMETERS</span></span>

### <span data-ttu-id="2e948-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e948-115">-AsJob</span></span>
<span data-ttu-id="2e948-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2e948-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e948-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e948-117">-DefaultProfile</span></span>
<span data-ttu-id="2e948-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e948-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e948-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2e948-119">-Force</span></span>
<span data-ttu-id="2e948-120">Fråga inte efter bekräftelse om du vill ta bort resursen</span><span class="sxs-lookup"><span data-stu-id="2e948-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="2e948-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e948-121">-InputObject</span></span>
<span data-ttu-id="2e948-122">Referens till VirtualNetworkTap-resursen</span><span class="sxs-lookup"><span data-stu-id="2e948-122">Reference to VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="2e948-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="2e948-123">-Name</span></span>
<span data-ttu-id="2e948-124">Namnet på tryckningen.</span><span class="sxs-lookup"><span data-stu-id="2e948-124">The name of the tap.</span></span>

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

### <span data-ttu-id="2e948-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e948-125">-PassThru</span></span>
<span data-ttu-id="2e948-126">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="2e948-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2e948-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2e948-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2e948-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e948-128">-ResourceGroupName</span></span>
<span data-ttu-id="2e948-129">Resurs grupps namnet för det virtuella nätverkets tryck.</span><span class="sxs-lookup"><span data-stu-id="2e948-129">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="2e948-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e948-130">-ResourceId</span></span>
<span data-ttu-id="2e948-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="2e948-131">VirtualNetworkTap resourceId</span></span>

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

### <span data-ttu-id="2e948-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2e948-132">-Confirm</span></span>
<span data-ttu-id="2e948-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2e948-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e948-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e948-134">-WhatIf</span></span>
<span data-ttu-id="2e948-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2e948-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e948-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2e948-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e948-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e948-137">CommonParameters</span></span>
<span data-ttu-id="2e948-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e948-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e948-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e948-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e948-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e948-140">INPUTS</span></span>

### <span data-ttu-id="2e948-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2e948-141">System.String</span></span>

### <span data-ttu-id="2e948-142">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2e948-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="2e948-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e948-143">OUTPUTS</span></span>

### <span data-ttu-id="2e948-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2e948-144">System.Boolean</span></span>

## <span data-ttu-id="2e948-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e948-145">NOTES</span></span>

## <span data-ttu-id="2e948-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e948-146">RELATED LINKS</span></span>

[<span data-ttu-id="2e948-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2e948-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="2e948-148">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2e948-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="2e948-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2e948-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
