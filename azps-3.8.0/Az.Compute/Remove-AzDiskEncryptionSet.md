---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928230"
---
# <span data-ttu-id="dd313-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="dd313-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="dd313-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd313-102">SYNOPSIS</span></span>
<span data-ttu-id="dd313-103">Tar bort en disk krypterings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="dd313-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="dd313-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd313-104">SYNTAX</span></span>

### <span data-ttu-id="dd313-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="dd313-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd313-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="dd313-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd313-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="dd313-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd313-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd313-108">DESCRIPTION</span></span>
<span data-ttu-id="dd313-109">Tar bort en disk krypterings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="dd313-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="dd313-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd313-110">EXAMPLES</span></span>

### <span data-ttu-id="dd313-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dd313-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="dd313-112">Ta bort disk krypterings uppsättningen ' enc1 ' i ' RG1 '</span><span class="sxs-lookup"><span data-stu-id="dd313-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="dd313-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd313-113">PARAMETERS</span></span>

### <span data-ttu-id="dd313-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd313-114">-AsJob</span></span>
<span data-ttu-id="dd313-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="dd313-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd313-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd313-116">-DefaultProfile</span></span>
<span data-ttu-id="dd313-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd313-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd313-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dd313-118">-Force</span></span>
<span data-ttu-id="dd313-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="dd313-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dd313-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd313-120">-InputObject</span></span>
<span data-ttu-id="dd313-121">Det lokala objektet i disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="dd313-121">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd313-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="dd313-122">-Name</span></span>
<span data-ttu-id="dd313-123">Namn på disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="dd313-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd313-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd313-124">-ResourceGroupName</span></span>
<span data-ttu-id="dd313-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="dd313-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd313-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd313-126">-ResourceId</span></span>
<span data-ttu-id="dd313-127">ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="dd313-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd313-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dd313-128">-Confirm</span></span>
<span data-ttu-id="dd313-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dd313-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd313-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd313-130">-WhatIf</span></span>
<span data-ttu-id="dd313-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dd313-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd313-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dd313-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd313-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd313-133">CommonParameters</span></span>
<span data-ttu-id="dd313-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd313-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd313-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd313-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd313-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd313-136">INPUTS</span></span>

### <span data-ttu-id="dd313-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dd313-137">System.String</span></span>

### <span data-ttu-id="dd313-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="dd313-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="dd313-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd313-139">OUTPUTS</span></span>

### <span data-ttu-id="dd313-140">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="dd313-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="dd313-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd313-141">NOTES</span></span>

## <span data-ttu-id="dd313-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd313-142">RELATED LINKS</span></span>
