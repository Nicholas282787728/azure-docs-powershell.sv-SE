---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 8e029309099b3f28c1a9f0108bf4e6f4a78cb45d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928254"
---
# <span data-ttu-id="a899d-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a899d-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="a899d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a899d-102">SYNOPSIS</span></span>
<span data-ttu-id="a899d-103">Tar bort en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="a899d-103">Removes a container service.</span></span>

## <span data-ttu-id="a899d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a899d-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a899d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a899d-105">DESCRIPTION</span></span>
<span data-ttu-id="a899d-106">Cmdleten **Remove-AzContainerService** tar bort en behållar tjänst från ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="a899d-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="a899d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a899d-107">EXAMPLES</span></span>

### <span data-ttu-id="a899d-108">Exempel 1: ta bort en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="a899d-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="a899d-109">Det här kommandot tar bort behållar tjänsten med namnet CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="a899d-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="a899d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a899d-110">PARAMETERS</span></span>

### <span data-ttu-id="a899d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a899d-111">-AsJob</span></span>
<span data-ttu-id="a899d-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="a899d-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a899d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a899d-113">-DefaultProfile</span></span>
<span data-ttu-id="a899d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a899d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a899d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a899d-115">-Force</span></span>
<span data-ttu-id="a899d-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a899d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a899d-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a899d-117">-Name</span></span>
<span data-ttu-id="a899d-118">Anger namnet på den behållar tjänst som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="a899d-118">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a899d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a899d-119">-ResourceGroupName</span></span>
<span data-ttu-id="a899d-120">Anger resurs gruppen för den behållar tjänst som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="a899d-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a899d-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a899d-121">-Confirm</span></span>
<span data-ttu-id="a899d-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a899d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a899d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a899d-123">-WhatIf</span></span>
<span data-ttu-id="a899d-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a899d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a899d-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a899d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a899d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a899d-126">CommonParameters</span></span>
<span data-ttu-id="a899d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a899d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a899d-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a899d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a899d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a899d-129">INPUTS</span></span>

### <span data-ttu-id="a899d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a899d-130">System.String</span></span>

## <span data-ttu-id="a899d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a899d-131">OUTPUTS</span></span>

### <span data-ttu-id="a899d-132">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a899d-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a899d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a899d-133">NOTES</span></span>

## <span data-ttu-id="a899d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a899d-134">RELATED LINKS</span></span>

[<span data-ttu-id="a899d-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a899d-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="a899d-136">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a899d-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="a899d-137">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a899d-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


