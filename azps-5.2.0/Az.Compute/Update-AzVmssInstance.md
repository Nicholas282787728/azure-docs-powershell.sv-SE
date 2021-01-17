---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: f7adb9ef086b233d44f2e5d9c6eb132669b102e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400960"
---
# <span data-ttu-id="d1ada-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="d1ada-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="d1ada-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1ada-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ada-103">Startar en manuell uppgradering av VMSS-instansen.</span><span class="sxs-lookup"><span data-stu-id="d1ada-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="d1ada-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1ada-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1ada-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1ada-105">DESCRIPTION</span></span>
<span data-ttu-id="d1ada-106">Update-AzVmssInstance cmdlet startar en manuell uppgradering av angiven virtuell dators (VMSS) instans.</span><span class="sxs-lookup"><span data-stu-id="d1ada-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="d1ada-107">Detta används när uppgraderings principen på VMSS skal uppsättning är inställd på manuell.</span><span class="sxs-lookup"><span data-stu-id="d1ada-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="d1ada-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1ada-108">EXAMPLES</span></span>

### <span data-ttu-id="d1ada-109">Exempel 1: starta en uppgradering av VMSS-instansen</span><span class="sxs-lookup"><span data-stu-id="d1ada-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="d1ada-110">Det här kommandot startar en uppgradering av VMSS med namnet VMScaleSet001 som har instans-ID 0.</span><span class="sxs-lookup"><span data-stu-id="d1ada-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="d1ada-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1ada-111">PARAMETERS</span></span>

### <span data-ttu-id="d1ada-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1ada-112">-AsJob</span></span>
<span data-ttu-id="d1ada-113">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="d1ada-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d1ada-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ada-114">-DefaultProfile</span></span>
<span data-ttu-id="d1ada-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ada-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1ada-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d1ada-116">-InstanceId</span></span>
<span data-ttu-id="d1ada-117">Anger, som en sträng mat ris, ID eller ID för den instans som ska uppgraderas.</span><span class="sxs-lookup"><span data-stu-id="d1ada-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ada-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1ada-118">-ResourceGroupName</span></span>
<span data-ttu-id="d1ada-119">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="d1ada-119">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ada-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d1ada-120">-VMScaleSetName</span></span>
<span data-ttu-id="d1ada-121">Anger namnet på den VMSS-instans som denna cmdlet uppgraderar.</span><span class="sxs-lookup"><span data-stu-id="d1ada-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ada-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d1ada-122">-Confirm</span></span>
<span data-ttu-id="d1ada-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d1ada-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ada-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1ada-124">-WhatIf</span></span>
<span data-ttu-id="d1ada-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d1ada-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1ada-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d1ada-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ada-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ada-127">CommonParameters</span></span>
<span data-ttu-id="d1ada-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ada-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ada-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1ada-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ada-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1ada-130">INPUTS</span></span>

### <span data-ttu-id="d1ada-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d1ada-131">System.String</span></span>

### <span data-ttu-id="d1ada-132">System. string []</span><span class="sxs-lookup"><span data-stu-id="d1ada-132">System.String[]</span></span>

## <span data-ttu-id="d1ada-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1ada-133">OUTPUTS</span></span>

### <span data-ttu-id="d1ada-134">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d1ada-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d1ada-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1ada-135">NOTES</span></span>

## <span data-ttu-id="d1ada-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1ada-136">RELATED LINKS</span></span>

[<span data-ttu-id="d1ada-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d1ada-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


