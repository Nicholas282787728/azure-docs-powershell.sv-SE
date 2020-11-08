---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261802"
---
# <span data-ttu-id="7f4d4-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7f4d4-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="7f4d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f4d4-102">SYNOPSIS</span></span>
<span data-ttu-id="7f4d4-103">Tar bort en Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="7f4d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f4d4-104">SYNTAX</span></span>

### <span data-ttu-id="7f4d4-105">ByVirtualWanName (standard)</span><span class="sxs-lookup"><span data-stu-id="7f4d4-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f4d4-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="7f4d4-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f4d4-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="7f4d4-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f4d4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f4d4-108">DESCRIPTION</span></span>
<span data-ttu-id="7f4d4-109">Tar bort en Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="7f4d4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f4d4-110">EXAMPLES</span></span>

### <span data-ttu-id="7f4d4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7f4d4-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="7f4d4-112">I det här exemplet skapas ett virtuellt WAN i en resurs grupp och sedan tas det omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="7f4d4-113">Om du inte vill att meddelandet ska visas när det virtuella WANet tas bort använder du flaggan-Force.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="7f4d4-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7f4d4-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="7f4d4-115">I det här exemplet skapas ett virtuellt WAN i en resurs grupp och sedan tas det omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="7f4d4-116">Denna borttagning sker med det virtuella WAN-objekt som returneras av New-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="7f4d4-117">Om du inte vill att meddelandet ska visas när det virtuella WANet tas bort använder du flaggan-Force.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="7f4d4-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7f4d4-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="7f4d4-119">I det här exemplet skapas ett virtuellt WAN i en resurs grupp och sedan tas det omedelbart bort.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="7f4d4-120">Den här borttagningen görs med den virtuella WAN Resource-ID som returneras av New-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="7f4d4-121">Om du inte vill att meddelandet ska visas när det virtuella WANet tas bort använder du flaggan-Force.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="7f4d4-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f4d4-122">PARAMETERS</span></span>

### <span data-ttu-id="7f4d4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f4d4-123">-DefaultProfile</span></span>
<span data-ttu-id="7f4d4-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f4d4-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7f4d4-125">-Force</span></span>
<span data-ttu-id="7f4d4-126">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7f4d4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f4d4-127">-InputObject</span></span>
<span data-ttu-id="7f4d4-128">Det virtuella WAN-objektet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-128">The virtual wan object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4d4-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="7f4d4-129">-Name</span></span>
<span data-ttu-id="7f4d4-130">Virtuellt WAN-namn.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-130">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f4d4-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f4d4-131">-PassThru</span></span>
<span data-ttu-id="7f4d4-132">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7f4d4-133">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7f4d4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f4d4-134">-ResourceGroupName</span></span>
<span data-ttu-id="7f4d4-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f4d4-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f4d4-136">-ResourceId</span></span>
<span data-ttu-id="7f4d4-137">Azure Resource ID för den virtuella WAN-tjänsten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4d4-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7f4d4-138">-Confirm</span></span>
<span data-ttu-id="7f4d4-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f4d4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f4d4-140">-WhatIf</span></span>
<span data-ttu-id="7f4d4-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f4d4-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f4d4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f4d4-143">CommonParameters</span></span>
<span data-ttu-id="7f4d4-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f4d4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f4d4-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f4d4-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f4d4-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f4d4-146">INPUTS</span></span>

### <span data-ttu-id="7f4d4-147">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7f4d4-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="7f4d4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7f4d4-148">System.String</span></span>

## <span data-ttu-id="7f4d4-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f4d4-149">OUTPUTS</span></span>

### <span data-ttu-id="7f4d4-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f4d4-150">System.Boolean</span></span>

## <span data-ttu-id="7f4d4-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f4d4-151">NOTES</span></span>

## <span data-ttu-id="7f4d4-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f4d4-152">RELATED LINKS</span></span>

[<span data-ttu-id="7f4d4-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7f4d4-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="7f4d4-154">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7f4d4-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="7f4d4-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="7f4d4-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
