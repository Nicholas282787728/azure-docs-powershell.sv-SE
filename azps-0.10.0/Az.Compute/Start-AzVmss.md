---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: d3677191bb3a196b97dcb8ff6c5b62b4aafd3a8b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923054"
---
# <span data-ttu-id="50164-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="50164-101">Start-AzVmss</span></span>

## <span data-ttu-id="50164-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50164-102">SYNOPSIS</span></span>
<span data-ttu-id="50164-103">Startar VMSS eller en uppsättning virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="50164-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="50164-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50164-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50164-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50164-105">DESCRIPTION</span></span>
<span data-ttu-id="50164-106">Cmdleten **Start-AzVmss** startar alla virtuella datorer inom den virtuella datorns skal uppsättning (VMSS) eller en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="50164-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="50164-107">Du kan använda parametern *InstanceID* för att välja en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="50164-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="50164-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50164-108">EXAMPLES</span></span>

### <span data-ttu-id="50164-109">Exempel 1: starta en specifik uppsättning virtuella datorer inom VMSS</span><span class="sxs-lookup"><span data-stu-id="50164-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="50164-110">Det här kommandot startar en specifik uppsättning virtuella datorer som anges med den instans-ID-sträng mat ris som tillhör VMSS som heter ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="50164-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="50164-111">Exempel 2: starta alla virtuella datorer inom VMSS</span><span class="sxs-lookup"><span data-stu-id="50164-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="50164-112">Det här kommandot startar alla virtuella datorer som tillhör VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="50164-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="50164-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50164-113">PARAMETERS</span></span>

### <span data-ttu-id="50164-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50164-114">-AsJob</span></span>
<span data-ttu-id="50164-115">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="50164-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="50164-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50164-116">-DefaultProfile</span></span>
<span data-ttu-id="50164-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50164-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50164-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="50164-118">-InstanceId</span></span>
<span data-ttu-id="50164-119">Anger, som en sträng mat ris, ID: t för de instanser som cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="50164-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="50164-120">Till exempel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="50164-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="50164-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50164-121">-ResourceGroupName</span></span>
<span data-ttu-id="50164-122">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="50164-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="50164-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="50164-123">-VMScaleSetName</span></span>
<span data-ttu-id="50164-124">Anger namnet på den VMSS som den här cmdleten startar för de virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="50164-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="50164-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50164-125">-Confirm</span></span>
<span data-ttu-id="50164-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50164-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50164-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50164-127">-WhatIf</span></span>
<span data-ttu-id="50164-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50164-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50164-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50164-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50164-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50164-130">CommonParameters</span></span>
<span data-ttu-id="50164-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50164-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50164-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50164-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50164-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50164-133">INPUTS</span></span>

### <span data-ttu-id="50164-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="50164-134">None</span></span>
<span data-ttu-id="50164-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="50164-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="50164-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50164-136">OUTPUTS</span></span>

###  
<span data-ttu-id="50164-137">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="50164-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="50164-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50164-138">NOTES</span></span>

## <span data-ttu-id="50164-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50164-139">RELATED LINKS</span></span>

[<span data-ttu-id="50164-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="50164-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="50164-141">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="50164-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="50164-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="50164-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="50164-143">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="50164-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="50164-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="50164-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="50164-145">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="50164-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="50164-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="50164-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


