---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: fc66151f39c969ebbdc9b54d6f6ed97db909e05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757797"
---
# <span data-ttu-id="92f0e-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="92f0e-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="92f0e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="92f0e-103">Tar bort en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="92f0e-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92f0e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92f0e-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92f0e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92f0e-105">DESCRIPTION</span></span>
<span data-ttu-id="92f0e-106">Cmdleten **Remove-AzureRmContainerService** tar bort en behållar tjänst från ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="92f0e-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="92f0e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92f0e-107">EXAMPLES</span></span>

### <span data-ttu-id="92f0e-108">Exempel 1: ta bort en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="92f0e-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="92f0e-109">Det här kommandot tar bort behållar tjänsten med namnet CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="92f0e-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="92f0e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92f0e-110">PARAMETERS</span></span>

### <span data-ttu-id="92f0e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f0e-111">-DefaultProfile</span></span>
<span data-ttu-id="92f0e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92f0e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92f0e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="92f0e-113">-Force</span></span>
<span data-ttu-id="92f0e-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="92f0e-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="92f0e-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="92f0e-115">-Name</span></span>
<span data-ttu-id="92f0e-116">Anger namnet på den behållar tjänst som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="92f0e-116">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="92f0e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f0e-117">-ResourceGroupName</span></span>
<span data-ttu-id="92f0e-118">Anger resurs gruppen för den behållar tjänst som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="92f0e-118">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="92f0e-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="92f0e-119">-Confirm</span></span>
<span data-ttu-id="92f0e-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92f0e-120">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="92f0e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92f0e-121">-WhatIf</span></span>
<span data-ttu-id="92f0e-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="92f0e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92f0e-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="92f0e-123">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="92f0e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f0e-124">CommonParameters</span></span>
<span data-ttu-id="92f0e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f0e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f0e-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92f0e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f0e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92f0e-127">INPUTS</span></span>

## <span data-ttu-id="92f0e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92f0e-128">OUTPUTS</span></span>

## <span data-ttu-id="92f0e-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92f0e-129">NOTES</span></span>

## <span data-ttu-id="92f0e-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92f0e-130">RELATED LINKS</span></span>

[<span data-ttu-id="92f0e-131">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="92f0e-131">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="92f0e-132">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="92f0e-132">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="92f0e-133">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="92f0e-133">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


