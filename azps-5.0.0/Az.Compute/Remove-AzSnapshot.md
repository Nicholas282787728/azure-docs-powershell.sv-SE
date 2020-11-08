---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 686f7dbe4bba17017e1920dd2c67a05c2ccd5eae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263443"
---
# <span data-ttu-id="b3693-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="b3693-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="b3693-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3693-102">SYNOPSIS</span></span>
<span data-ttu-id="b3693-103">Tar bort en stillbild.</span><span class="sxs-lookup"><span data-stu-id="b3693-103">Removes a snapshot.</span></span>

## <span data-ttu-id="b3693-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3693-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3693-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3693-105">DESCRIPTION</span></span>
<span data-ttu-id="b3693-106">Cmdleten **Remove-AzSnapshot** tar bort en stillbild.</span><span class="sxs-lookup"><span data-stu-id="b3693-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="b3693-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3693-107">EXAMPLES</span></span>

### <span data-ttu-id="b3693-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b3693-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="b3693-109">Det här kommandot tar bort stillbilden "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b3693-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b3693-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3693-110">PARAMETERS</span></span>

### <span data-ttu-id="b3693-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3693-111">-AsJob</span></span>
<span data-ttu-id="b3693-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="b3693-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b3693-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3693-113">-DefaultProfile</span></span>
<span data-ttu-id="b3693-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3693-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3693-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b3693-115">-Force</span></span>
<span data-ttu-id="b3693-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b3693-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b3693-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3693-117">-ResourceGroupName</span></span>
<span data-ttu-id="b3693-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b3693-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b3693-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="b3693-119">-SnapshotName</span></span>
<span data-ttu-id="b3693-120">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="b3693-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="b3693-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b3693-121">-Confirm</span></span>
<span data-ttu-id="b3693-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b3693-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3693-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3693-123">-WhatIf</span></span>
<span data-ttu-id="b3693-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b3693-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3693-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b3693-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3693-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3693-126">CommonParameters</span></span>
<span data-ttu-id="b3693-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3693-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3693-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3693-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3693-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3693-129">INPUTS</span></span>

### <span data-ttu-id="b3693-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b3693-130">System.String</span></span>

## <span data-ttu-id="b3693-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3693-131">OUTPUTS</span></span>

### <span data-ttu-id="b3693-132">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b3693-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b3693-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3693-133">NOTES</span></span>

## <span data-ttu-id="b3693-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3693-134">RELATED LINKS</span></span>
