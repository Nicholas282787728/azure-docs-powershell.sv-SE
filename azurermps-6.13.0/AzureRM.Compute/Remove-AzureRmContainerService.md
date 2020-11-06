---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: 19c94fae0192766b87f430e6137fe8d3652325c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575276"
---
# <span data-ttu-id="59630-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="59630-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="59630-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59630-102">SYNOPSIS</span></span>
<span data-ttu-id="59630-103">Tar bort en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="59630-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59630-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59630-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59630-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59630-105">DESCRIPTION</span></span>
<span data-ttu-id="59630-106">Cmdleten **Remove-AzureRmContainerService** tar bort en behållar tjänst från ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="59630-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="59630-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59630-107">EXAMPLES</span></span>

### <span data-ttu-id="59630-108">Exempel 1: ta bort en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="59630-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="59630-109">Det här kommandot tar bort behållar tjänsten med namnet CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="59630-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="59630-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59630-110">PARAMETERS</span></span>

### <span data-ttu-id="59630-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59630-111">-AsJob</span></span>
<span data-ttu-id="59630-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="59630-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="59630-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59630-113">-DefaultProfile</span></span>
<span data-ttu-id="59630-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59630-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59630-115">-Force</span><span class="sxs-lookup"><span data-stu-id="59630-115">-Force</span></span>
<span data-ttu-id="59630-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="59630-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="59630-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="59630-117">-Name</span></span>
<span data-ttu-id="59630-118">Anger namnet på den behållar tjänst som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="59630-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59630-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59630-119">-ResourceGroupName</span></span>
<span data-ttu-id="59630-120">Anger resurs gruppen för den behållar tjänst som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="59630-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="59630-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59630-121">-Confirm</span></span>
<span data-ttu-id="59630-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59630-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59630-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59630-123">-WhatIf</span></span>
<span data-ttu-id="59630-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59630-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59630-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59630-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59630-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59630-126">CommonParameters</span></span>
<span data-ttu-id="59630-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59630-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59630-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59630-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59630-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59630-129">INPUTS</span></span>

### <span data-ttu-id="59630-130">System. String</span><span class="sxs-lookup"><span data-stu-id="59630-130">System.String</span></span>

## <span data-ttu-id="59630-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59630-131">OUTPUTS</span></span>

### <span data-ttu-id="59630-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="59630-132">System.Void</span></span>

## <span data-ttu-id="59630-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59630-133">NOTES</span></span>

## <span data-ttu-id="59630-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59630-134">RELATED LINKS</span></span>

[<span data-ttu-id="59630-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="59630-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="59630-136">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="59630-136">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="59630-137">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="59630-137">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


