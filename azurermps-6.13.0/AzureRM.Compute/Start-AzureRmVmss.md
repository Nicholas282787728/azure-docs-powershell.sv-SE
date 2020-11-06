---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 131fec8efa9075640d367726e5178caa54b9402a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572879"
---
# <span data-ttu-id="c3122-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3122-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="c3122-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3122-102">SYNOPSIS</span></span>
<span data-ttu-id="c3122-103">Startar VMSS eller en uppsättning virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="c3122-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3122-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3122-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3122-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3122-105">DESCRIPTION</span></span>
<span data-ttu-id="c3122-106">Cmdleten **Start-AzureRmVmss** startar alla virtuella datorer inom den virtuella datorns skal uppsättning (VMSS) eller en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="c3122-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="c3122-107">Du kan använda parametern *InstanceID* för att välja en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="c3122-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="c3122-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3122-108">EXAMPLES</span></span>

### <span data-ttu-id="c3122-109">Exempel 1: starta en specifik uppsättning virtuella datorer inom VMSS</span><span class="sxs-lookup"><span data-stu-id="c3122-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="c3122-110">Det här kommandot startar en specifik uppsättning virtuella datorer som anges med den instans-ID-sträng mat ris som tillhör VMSS som heter ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="c3122-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="c3122-111">Exempel 2: starta alla virtuella datorer inom VMSS</span><span class="sxs-lookup"><span data-stu-id="c3122-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="c3122-112">Det här kommandot startar alla virtuella datorer som tillhör VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="c3122-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="c3122-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3122-113">PARAMETERS</span></span>

### <span data-ttu-id="c3122-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3122-114">-AsJob</span></span>
<span data-ttu-id="c3122-115">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="c3122-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c3122-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3122-116">-DefaultProfile</span></span>
<span data-ttu-id="c3122-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3122-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3122-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c3122-118">-InstanceId</span></span>
<span data-ttu-id="c3122-119">Anger, som en sträng mat ris, ID: t för de instanser som cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="c3122-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="c3122-120">Till exempel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="c3122-120">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3122-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3122-121">-ResourceGroupName</span></span>
<span data-ttu-id="c3122-122">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="c3122-122">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3122-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c3122-123">-VMScaleSetName</span></span>
<span data-ttu-id="c3122-124">Anger namnet på den VMSS som den här cmdleten startar för de virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="c3122-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3122-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3122-125">-Confirm</span></span>
<span data-ttu-id="c3122-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3122-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3122-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3122-127">-WhatIf</span></span>
<span data-ttu-id="c3122-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3122-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3122-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3122-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3122-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3122-130">CommonParameters</span></span>
<span data-ttu-id="c3122-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3122-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3122-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3122-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3122-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3122-133">INPUTS</span></span>

### <span data-ttu-id="c3122-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c3122-134">System.String</span></span>

### <span data-ttu-id="c3122-135">System. string []</span><span class="sxs-lookup"><span data-stu-id="c3122-135">System.String[]</span></span>

## <span data-ttu-id="c3122-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3122-136">OUTPUTS</span></span>

### <span data-ttu-id="c3122-137">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c3122-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c3122-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3122-138">NOTES</span></span>

## <span data-ttu-id="c3122-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3122-139">RELATED LINKS</span></span>

[<span data-ttu-id="c3122-140">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3122-140">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="c3122-141">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3122-141">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="c3122-142">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3122-142">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="c3122-143">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3122-143">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="c3122-144">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3122-144">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="c3122-145">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3122-145">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="c3122-146">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c3122-146">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


