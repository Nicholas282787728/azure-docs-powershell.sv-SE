---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 6b3291a77f7c69372124b8c0de2ba78c8810f02b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756358"
---
# <span data-ttu-id="83e25-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="83e25-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="83e25-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83e25-102">SYNOPSIS</span></span>
<span data-ttu-id="83e25-103">Startar VMSS eller en uppsättning virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="83e25-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83e25-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83e25-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83e25-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83e25-105">DESCRIPTION</span></span>
<span data-ttu-id="83e25-106">Cmdleten **Start-AzureRmVmss** startar alla virtuella datorer inom den virtuella datorns skal uppsättning (VMSS) eller en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="83e25-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="83e25-107">Du kan använda parametern *InstanceID* för att välja en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="83e25-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="83e25-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83e25-108">EXAMPLES</span></span>

### <span data-ttu-id="83e25-109">Exempel 1: starta en specifik uppsättning virtuella datorer inom VMSS</span><span class="sxs-lookup"><span data-stu-id="83e25-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="83e25-110">Det här kommandot startar en specifik uppsättning virtuella datorer som anges med den instans-ID-sträng mat ris som tillhör VMSS som heter ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="83e25-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="83e25-111">Exempel 2: starta alla virtuella datorer inom VMSS</span><span class="sxs-lookup"><span data-stu-id="83e25-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="83e25-112">Det här kommandot startar alla virtuella datorer som tillhör VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="83e25-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="83e25-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83e25-113">PARAMETERS</span></span>

### <span data-ttu-id="83e25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e25-114">-DefaultProfile</span></span>
<span data-ttu-id="83e25-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83e25-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83e25-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="83e25-116">-InstanceId</span></span>
<span data-ttu-id="83e25-117">Anger, som en sträng mat ris, ID: t för de instanser som cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="83e25-117">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="83e25-118">Till exempel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="83e25-118">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="83e25-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83e25-119">-ResourceGroupName</span></span>
<span data-ttu-id="83e25-120">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="83e25-120">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="83e25-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="83e25-121">-VMScaleSetName</span></span>
<span data-ttu-id="83e25-122">Anger namnet på den VMSS som den här cmdleten startar för de virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="83e25-122">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="83e25-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="83e25-123">-Confirm</span></span>
<span data-ttu-id="83e25-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83e25-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83e25-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83e25-125">-WhatIf</span></span>
<span data-ttu-id="83e25-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="83e25-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83e25-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="83e25-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83e25-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e25-128">CommonParameters</span></span>
<span data-ttu-id="83e25-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83e25-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e25-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83e25-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e25-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83e25-131">INPUTS</span></span>

## <span data-ttu-id="83e25-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83e25-132">OUTPUTS</span></span>

###  
<span data-ttu-id="83e25-133">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="83e25-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="83e25-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83e25-134">NOTES</span></span>

## <span data-ttu-id="83e25-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83e25-135">RELATED LINKS</span></span>

[<span data-ttu-id="83e25-136">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="83e25-136">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="83e25-137">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="83e25-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="83e25-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="83e25-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="83e25-139">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="83e25-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="83e25-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="83e25-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="83e25-141">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="83e25-141">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="83e25-142">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="83e25-142">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


