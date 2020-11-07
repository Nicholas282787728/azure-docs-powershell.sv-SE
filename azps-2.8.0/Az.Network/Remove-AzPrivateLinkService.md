---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 3b0ba9527ca7d0354429a90439bbe33d973bf550
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918041"
---
# <span data-ttu-id="97cad-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="97cad-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="97cad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97cad-102">SYNOPSIS</span></span>
<span data-ttu-id="97cad-103">Tar bort en privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="97cad-103">Removes a private link service</span></span>

## <span data-ttu-id="97cad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97cad-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97cad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97cad-105">DESCRIPTION</span></span>
<span data-ttu-id="97cad-106">Cmdleten **Remove-AzPrivateLinkService** tar bort en privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="97cad-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="97cad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97cad-107">EXAMPLES</span></span>

### <span data-ttu-id="97cad-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="97cad-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="97cad-109">I det här exemplet tas en privat länk tjänst bort med namnet TestPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="97cad-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="97cad-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97cad-110">PARAMETERS</span></span>

### <span data-ttu-id="97cad-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97cad-111">-AsJob</span></span>
<span data-ttu-id="97cad-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="97cad-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97cad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97cad-113">-DefaultProfile</span></span>
<span data-ttu-id="97cad-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97cad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97cad-115">-Force</span><span class="sxs-lookup"><span data-stu-id="97cad-115">-Force</span></span>
<span data-ttu-id="97cad-116">Fråga inte efter bekräftelse om du vill ta bort resursen</span><span class="sxs-lookup"><span data-stu-id="97cad-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="97cad-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="97cad-117">-Name</span></span>
<span data-ttu-id="97cad-118">Namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="97cad-118">The name of the service.</span></span>

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

### <span data-ttu-id="97cad-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97cad-119">-PassThru</span></span>
<span data-ttu-id="97cad-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="97cad-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="97cad-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="97cad-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="97cad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97cad-122">-ResourceGroupName</span></span>
<span data-ttu-id="97cad-123">Namnet på den privata länk tjänsten.</span><span class="sxs-lookup"><span data-stu-id="97cad-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="97cad-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97cad-124">-Confirm</span></span>
<span data-ttu-id="97cad-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97cad-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97cad-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97cad-126">-WhatIf</span></span>
<span data-ttu-id="97cad-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97cad-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97cad-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97cad-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97cad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97cad-129">CommonParameters</span></span>
<span data-ttu-id="97cad-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97cad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97cad-131">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97cad-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97cad-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97cad-132">INPUTS</span></span>

### <span data-ttu-id="97cad-133">System. String</span><span class="sxs-lookup"><span data-stu-id="97cad-133">System.String</span></span>

## <span data-ttu-id="97cad-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97cad-134">OUTPUTS</span></span>

### <span data-ttu-id="97cad-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97cad-135">System.Boolean</span></span>

## <span data-ttu-id="97cad-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97cad-136">NOTES</span></span>

## <span data-ttu-id="97cad-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97cad-137">RELATED LINKS</span></span>

[<span data-ttu-id="97cad-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="97cad-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="97cad-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="97cad-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)