---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: 30029a6fbd14a7e94ffe60f058405a2907b1cb53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575274"
---
# <span data-ttu-id="2f577-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="2f577-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="2f577-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f577-102">SYNOPSIS</span></span>
<span data-ttu-id="2f577-103">Tar bort en disk.</span><span class="sxs-lookup"><span data-stu-id="2f577-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f577-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f577-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f577-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f577-105">DESCRIPTION</span></span>
<span data-ttu-id="2f577-106">Cmdleten **Remove-AzureRmDisk** tar bort en disk.</span><span class="sxs-lookup"><span data-stu-id="2f577-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="2f577-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f577-107">EXAMPLES</span></span>

### <span data-ttu-id="2f577-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2f577-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="2f577-109">Det här kommandot tar bort disken "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2f577-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="2f577-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f577-110">PARAMETERS</span></span>

### <span data-ttu-id="2f577-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f577-111">-AsJob</span></span>
<span data-ttu-id="2f577-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="2f577-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2f577-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f577-113">-DefaultProfile</span></span>
<span data-ttu-id="2f577-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f577-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f577-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="2f577-115">-DiskName</span></span>
<span data-ttu-id="2f577-116">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="2f577-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="2f577-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2f577-117">-Force</span></span>
<span data-ttu-id="2f577-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2f577-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2f577-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f577-119">-ResourceGroupName</span></span>
<span data-ttu-id="2f577-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2f577-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2f577-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2f577-121">-Confirm</span></span>
<span data-ttu-id="2f577-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f577-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f577-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f577-123">-WhatIf</span></span>
<span data-ttu-id="2f577-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2f577-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f577-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2f577-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f577-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f577-126">CommonParameters</span></span>
<span data-ttu-id="2f577-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f577-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f577-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f577-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f577-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f577-129">INPUTS</span></span>

### <span data-ttu-id="2f577-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2f577-130">System.String</span></span>

## <span data-ttu-id="2f577-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f577-131">OUTPUTS</span></span>

### <span data-ttu-id="2f577-132">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2f577-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2f577-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f577-133">NOTES</span></span>

## <span data-ttu-id="2f577-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f577-134">RELATED LINKS</span></span>
