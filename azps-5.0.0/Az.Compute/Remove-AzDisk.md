---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: d48946b39c27a203e7d119c69e965633de8c6d6d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271173"
---
# <span data-ttu-id="eaad3-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="eaad3-101">Remove-AzDisk</span></span>

## <span data-ttu-id="eaad3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eaad3-102">SYNOPSIS</span></span>
<span data-ttu-id="eaad3-103">Tar bort en disk.</span><span class="sxs-lookup"><span data-stu-id="eaad3-103">Removes a disk.</span></span>

## <span data-ttu-id="eaad3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eaad3-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaad3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eaad3-105">DESCRIPTION</span></span>
<span data-ttu-id="eaad3-106">Cmdleten **Remove-AzDisk** tar bort en disk.</span><span class="sxs-lookup"><span data-stu-id="eaad3-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="eaad3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eaad3-107">EXAMPLES</span></span>

### <span data-ttu-id="eaad3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eaad3-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="eaad3-109">Det här kommandot tar bort disken "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="eaad3-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="eaad3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eaad3-110">PARAMETERS</span></span>

### <span data-ttu-id="eaad3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eaad3-111">-AsJob</span></span>
<span data-ttu-id="eaad3-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="eaad3-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="eaad3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaad3-113">-DefaultProfile</span></span>
<span data-ttu-id="eaad3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eaad3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaad3-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="eaad3-115">-DiskName</span></span>
<span data-ttu-id="eaad3-116">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="eaad3-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="eaad3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="eaad3-117">-Force</span></span>
<span data-ttu-id="eaad3-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="eaad3-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eaad3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaad3-119">-ResourceGroupName</span></span>
<span data-ttu-id="eaad3-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="eaad3-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="eaad3-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eaad3-121">-Confirm</span></span>
<span data-ttu-id="eaad3-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eaad3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaad3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaad3-123">-WhatIf</span></span>
<span data-ttu-id="eaad3-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eaad3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaad3-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eaad3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaad3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaad3-126">CommonParameters</span></span>
<span data-ttu-id="eaad3-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaad3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaad3-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eaad3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaad3-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eaad3-129">INPUTS</span></span>

### <span data-ttu-id="eaad3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eaad3-130">System.String</span></span>

## <span data-ttu-id="eaad3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eaad3-131">OUTPUTS</span></span>

### <span data-ttu-id="eaad3-132">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="eaad3-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="eaad3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eaad3-133">NOTES</span></span>

## <span data-ttu-id="eaad3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eaad3-134">RELATED LINKS</span></span>
