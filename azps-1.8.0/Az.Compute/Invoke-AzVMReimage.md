---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 6c8744d68abfab882e56b0b7e33674d48232c900
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917394"
---
# <span data-ttu-id="e15cb-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="e15cb-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="e15cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e15cb-102">SYNOPSIS</span></span>
<span data-ttu-id="e15cb-103">Bild av en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="e15cb-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="e15cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e15cb-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e15cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e15cb-105">DESCRIPTION</span></span>
<span data-ttu-id="e15cb-106">Cmdleten **Invoke-AzVMReimage** avbildningar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="e15cb-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="e15cb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e15cb-107">EXAMPLES</span></span>

### <span data-ttu-id="e15cb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e15cb-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="e15cb-109">Det här kommandot återsätter den virtuella datorn som heter VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e15cb-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="e15cb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e15cb-110">PARAMETERS</span></span>

### <span data-ttu-id="e15cb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e15cb-111">-AsJob</span></span>
<span data-ttu-id="e15cb-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e15cb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e15cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e15cb-113">-DefaultProfile</span></span>
<span data-ttu-id="e15cb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e15cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e15cb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e15cb-115">-ResourceGroupName</span></span>
<span data-ttu-id="e15cb-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e15cb-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e15cb-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="e15cb-117">-TempDisk</span></span>
<span data-ttu-id="e15cb-118">Anger om du vill att bilden ska visas igen.</span><span class="sxs-lookup"><span data-stu-id="e15cb-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="e15cb-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="e15cb-119">-VMName</span></span>
<span data-ttu-id="e15cb-120">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="e15cb-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="e15cb-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e15cb-121">-Confirm</span></span>
<span data-ttu-id="e15cb-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e15cb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e15cb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e15cb-123">-WhatIf</span></span>
<span data-ttu-id="e15cb-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e15cb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e15cb-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e15cb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e15cb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e15cb-126">CommonParameters</span></span>
<span data-ttu-id="e15cb-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e15cb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e15cb-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e15cb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e15cb-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e15cb-129">INPUTS</span></span>

### <span data-ttu-id="e15cb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e15cb-130">System.String</span></span>

## <span data-ttu-id="e15cb-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e15cb-131">OUTPUTS</span></span>

### <span data-ttu-id="e15cb-132">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e15cb-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e15cb-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e15cb-133">NOTES</span></span>

## <span data-ttu-id="e15cb-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e15cb-134">RELATED LINKS</span></span>
