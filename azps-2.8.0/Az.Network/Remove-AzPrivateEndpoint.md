---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 1ad9ff225871cde9104a346bd758f2716f630bc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918037"
---
# <span data-ttu-id="e8b3b-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8b3b-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="e8b3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b3b-103">Tar bort en privat slut punkt.</span><span class="sxs-lookup"><span data-stu-id="e8b3b-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="e8b3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8b3b-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8b3b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8b3b-105">DESCRIPTION</span></span>
<span data-ttu-id="e8b3b-106">Cmdleten **Remove-AzPrivateEndpoint** tar bort en privat slut punkt.</span><span class="sxs-lookup"><span data-stu-id="e8b3b-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="e8b3b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8b3b-107">EXAMPLES</span></span>

### <span data-ttu-id="e8b3b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e8b3b-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="e8b3b-109">Det här exemplet tar bort en privat slut punkt med namnet MyPrivateEndpoint1.</span><span class="sxs-lookup"><span data-stu-id="e8b3b-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="e8b3b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8b3b-110">PARAMETERS</span></span>

### <span data-ttu-id="e8b3b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8b3b-111">-AsJob</span></span>
<span data-ttu-id="e8b3b-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e8b3b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8b3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8b3b-113">-DefaultProfile</span></span>
<span data-ttu-id="e8b3b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e8b3b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8b3b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e8b3b-115">-Force</span></span>
<span data-ttu-id="e8b3b-116">Fråga inte efter bekräftelse om du vill ta bort resursen</span><span class="sxs-lookup"><span data-stu-id="e8b3b-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="e8b3b-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e8b3b-117">-Name</span></span>
<span data-ttu-id="e8b3b-118">Namnet på den privata slut punkten.</span><span class="sxs-lookup"><span data-stu-id="e8b3b-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b3b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8b3b-119">-PassThru</span></span>
<span data-ttu-id="e8b3b-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="e8b3b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e8b3b-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e8b3b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e8b3b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8b3b-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8b3b-123">Namnet på den privata slut punkten för resursen.</span><span class="sxs-lookup"><span data-stu-id="e8b3b-123">The resource group name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b3b-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e8b3b-124">-Confirm</span></span>
<span data-ttu-id="e8b3b-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e8b3b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8b3b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8b3b-126">-WhatIf</span></span>
<span data-ttu-id="e8b3b-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e8b3b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8b3b-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e8b3b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8b3b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b3b-129">CommonParameters</span></span>
<span data-ttu-id="e8b3b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8b3b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b3b-131">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8b3b-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b3b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8b3b-132">INPUTS</span></span>

### <span data-ttu-id="e8b3b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e8b3b-133">System.String</span></span>

## <span data-ttu-id="e8b3b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8b3b-134">OUTPUTS</span></span>

### <span data-ttu-id="e8b3b-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8b3b-135">System.Boolean</span></span>

## <span data-ttu-id="e8b3b-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8b3b-136">NOTES</span></span>

## <span data-ttu-id="e8b3b-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8b3b-137">RELATED LINKS</span></span>

[<span data-ttu-id="e8b3b-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8b3b-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="e8b3b-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8b3b-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)