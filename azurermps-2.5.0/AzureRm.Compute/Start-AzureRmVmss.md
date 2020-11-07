---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2135b6244453cb7d958871c23b64016404d02502
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930998"
---
# <span data-ttu-id="d4cfc-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4cfc-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="d4cfc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="d4cfc-103">Startar VMSS eller en uppsättning virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4cfc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4cfc-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4cfc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4cfc-105">DESCRIPTION</span></span>
<span data-ttu-id="d4cfc-106">Cmdleten **Start-AzureRmVmss** startar alla virtuella datorer inom den virtuella datorns skal uppsättning (VMSS) eller en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="d4cfc-107">Du kan använda parametern *InstanceID* för att välja en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="d4cfc-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4cfc-108">EXAMPLES</span></span>

### <span data-ttu-id="d4cfc-109">Exempel 1: starta en specifik uppsättning virtuella datorer inom VMSS</span><span class="sxs-lookup"><span data-stu-id="d4cfc-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="d4cfc-110">Det här kommandot startar en specifik uppsättning virtuella datorer som anges med den instans-ID-sträng mat ris som tillhör VMSS som heter ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="d4cfc-111">Exempel 2: starta alla virtuella datorer inom VMSS</span><span class="sxs-lookup"><span data-stu-id="d4cfc-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="d4cfc-112">Det här kommandot startar alla virtuella datorer som tillhör VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="d4cfc-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4cfc-113">PARAMETERS</span></span>

### <span data-ttu-id="d4cfc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4cfc-114">-AsJob</span></span>
<span data-ttu-id="d4cfc-115">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d4cfc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4cfc-116">-DefaultProfile</span></span>
<span data-ttu-id="d4cfc-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4cfc-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d4cfc-118">-InstanceId</span></span>
<span data-ttu-id="d4cfc-119">Anger, som en sträng mat ris, ID: t för de instanser som cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="d4cfc-120">Till exempel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="d4cfc-120">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4cfc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4cfc-121">-ResourceGroupName</span></span>
<span data-ttu-id="d4cfc-122">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-122">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4cfc-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d4cfc-123">-VMScaleSetName</span></span>
<span data-ttu-id="d4cfc-124">Anger namnet på den VMSS som den här cmdleten startar för de virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4cfc-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d4cfc-125">-Confirm</span></span>
<span data-ttu-id="d4cfc-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4cfc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4cfc-127">-WhatIf</span></span>
<span data-ttu-id="d4cfc-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4cfc-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4cfc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4cfc-130">CommonParameters</span></span>
<span data-ttu-id="d4cfc-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4cfc-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4cfc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4cfc-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4cfc-133">INPUTS</span></span>

### <span data-ttu-id="d4cfc-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="d4cfc-134">None</span></span>
<span data-ttu-id="d4cfc-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d4cfc-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4cfc-136">OUTPUTS</span></span>

###  
<span data-ttu-id="d4cfc-137">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d4cfc-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d4cfc-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4cfc-138">NOTES</span></span>

## <span data-ttu-id="d4cfc-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4cfc-139">RELATED LINKS</span></span>

[<span data-ttu-id="d4cfc-140">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4cfc-140">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="d4cfc-141">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4cfc-141">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="d4cfc-142">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4cfc-142">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="d4cfc-143">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4cfc-143">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="d4cfc-144">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4cfc-144">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="d4cfc-145">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4cfc-145">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="d4cfc-146">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4cfc-146">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


