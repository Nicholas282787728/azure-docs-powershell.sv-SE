---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 4b95610996aad93144ccaa749c41319cf513ff7f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416064"
---
# <span data-ttu-id="b4832-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b4832-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="b4832-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4832-102">SYNOPSIS</span></span>
<span data-ttu-id="b4832-103">Tar bort en privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="b4832-103">Removes a private link service</span></span>

## <span data-ttu-id="b4832-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4832-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4832-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4832-105">DESCRIPTION</span></span>
<span data-ttu-id="b4832-106">Cmdleten **Remove-AzPrivateLinkService** tar bort en privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="b4832-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="b4832-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4832-107">EXAMPLES</span></span>

### <span data-ttu-id="b4832-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b4832-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="b4832-109">I det här exemplet tas en privat länk tjänst bort med namnet TestPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="b4832-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="b4832-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4832-110">PARAMETERS</span></span>

### <span data-ttu-id="b4832-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4832-111">-AsJob</span></span>
<span data-ttu-id="b4832-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b4832-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4832-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4832-113">-DefaultProfile</span></span>
<span data-ttu-id="b4832-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4832-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4832-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b4832-115">-Force</span></span>
<span data-ttu-id="b4832-116">Fråga inte efter bekräftelse om du vill ta bort resursen</span><span class="sxs-lookup"><span data-stu-id="b4832-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="b4832-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4832-117">-Name</span></span>
<span data-ttu-id="b4832-118">Namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b4832-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4832-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4832-119">-PassThru</span></span>
<span data-ttu-id="b4832-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="b4832-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b4832-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b4832-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b4832-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4832-122">-ResourceGroupName</span></span>
<span data-ttu-id="b4832-123">Namnet på den privata länk tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b4832-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="b4832-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b4832-124">-Confirm</span></span>
<span data-ttu-id="b4832-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b4832-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4832-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4832-126">-WhatIf</span></span>
<span data-ttu-id="b4832-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b4832-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4832-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b4832-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4832-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4832-129">CommonParameters</span></span>
<span data-ttu-id="b4832-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4832-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4832-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4832-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4832-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4832-132">INPUTS</span></span>

### <span data-ttu-id="b4832-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b4832-133">System.String</span></span>

## <span data-ttu-id="b4832-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4832-134">OUTPUTS</span></span>

### <span data-ttu-id="b4832-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4832-135">System.Boolean</span></span>

## <span data-ttu-id="b4832-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4832-136">NOTES</span></span>

## <span data-ttu-id="b4832-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4832-137">RELATED LINKS</span></span>

[<span data-ttu-id="b4832-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b4832-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="b4832-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b4832-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)