---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 116cffabc942572db48d6f86b469a954bccbc1c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102106"
---
# <span data-ttu-id="2581f-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2581f-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="2581f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2581f-102">SYNOPSIS</span></span>
<span data-ttu-id="2581f-103">Tar bort en Azure VirtualHub-resurs.</span><span class="sxs-lookup"><span data-stu-id="2581f-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="2581f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2581f-104">SYNTAX</span></span>

### <span data-ttu-id="2581f-105">ByVirtualHubName (standard)</span><span class="sxs-lookup"><span data-stu-id="2581f-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2581f-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="2581f-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2581f-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="2581f-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2581f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2581f-108">DESCRIPTION</span></span>
<span data-ttu-id="2581f-109">Tar bort en Azure VirtualHub-resurs.</span><span class="sxs-lookup"><span data-stu-id="2581f-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="2581f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2581f-110">EXAMPLES</span></span>

### <span data-ttu-id="2581f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2581f-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="2581f-112">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="2581f-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="2581f-113">Det virtuella navet har adress utrymmet "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="2581f-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="2581f-114">Då raderas den virtuella navet med dess ResourceGroupName och ResourceName.</span><span class="sxs-lookup"><span data-stu-id="2581f-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="2581f-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2581f-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="2581f-116">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="2581f-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="2581f-117">Det virtuella navet har adress utrymmet "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="2581f-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="2581f-118">Sedan raderas det virtuella navet med ett indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="2581f-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="2581f-119">Indatavärdet är av typen PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="2581f-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="2581f-120">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="2581f-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="2581f-121">Ovanstående skapar en resurs grupp "testRG", ett virtuellt WAN och ett virtuellt nav i West i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="2581f-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="2581f-122">Det virtuella navet har adress utrymmet "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="2581f-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="2581f-123">Sedan raderas den virtuella navet med PowerShell-ledning med utdata från get-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="2581f-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="2581f-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2581f-124">PARAMETERS</span></span>

### <span data-ttu-id="2581f-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2581f-125">-AsJob</span></span>
<span data-ttu-id="2581f-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2581f-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2581f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2581f-127">-DefaultProfile</span></span>
<span data-ttu-id="2581f-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2581f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2581f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="2581f-129">-Force</span></span>
<span data-ttu-id="2581f-130">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="2581f-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2581f-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2581f-131">-InputObject</span></span>
<span data-ttu-id="2581f-132">Det virtuella nav-objekt som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="2581f-132">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2581f-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="2581f-133">-Name</span></span>
<span data-ttu-id="2581f-134">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="2581f-134">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2581f-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2581f-135">-PassThru</span></span>
<span data-ttu-id="2581f-136">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="2581f-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2581f-137">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2581f-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2581f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2581f-138">-ResourceGroupName</span></span>
<span data-ttu-id="2581f-139">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2581f-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2581f-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2581f-140">-ResourceId</span></span>
<span data-ttu-id="2581f-141">Resurs-ID för det virtuella nav som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="2581f-141">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2581f-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2581f-142">-Confirm</span></span>
<span data-ttu-id="2581f-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2581f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2581f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2581f-144">-WhatIf</span></span>
<span data-ttu-id="2581f-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2581f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2581f-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2581f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2581f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2581f-147">CommonParameters</span></span>
<span data-ttu-id="2581f-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2581f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2581f-149">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2581f-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2581f-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2581f-150">INPUTS</span></span>

### <span data-ttu-id="2581f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="2581f-151">System.String</span></span>

### <span data-ttu-id="2581f-152">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2581f-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="2581f-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2581f-153">OUTPUTS</span></span>

### <span data-ttu-id="2581f-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2581f-154">System.Boolean</span></span>

## <span data-ttu-id="2581f-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2581f-155">NOTES</span></span>

## <span data-ttu-id="2581f-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2581f-156">RELATED LINKS</span></span>

[<span data-ttu-id="2581f-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2581f-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="2581f-158">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2581f-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="2581f-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2581f-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
