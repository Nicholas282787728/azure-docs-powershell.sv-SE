---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090644"
---
# <span data-ttu-id="d3387-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d3387-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="d3387-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3387-102">SYNOPSIS</span></span>
<span data-ttu-id="d3387-103">Ta bort en routningsregler från platsen.</span><span class="sxs-lookup"><span data-stu-id="d3387-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="d3387-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3387-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3387-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3387-105">DESCRIPTION</span></span>
<span data-ttu-id="d3387-106">Cmdleten **Remove-AzWebAppTrafficRouting** tar bort en routningsregler från en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="d3387-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="d3387-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3387-107">EXAMPLES</span></span>

### <span data-ttu-id="d3387-108">Exempel 1 tar bort den specifika regeln för routning från webapp-platsen</span><span class="sxs-lookup"><span data-stu-id="d3387-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="d3387-109">Det här kommandot tar bort en routningsregler för en viss webapp-plats.</span><span class="sxs-lookup"><span data-stu-id="d3387-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="d3387-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3387-110">PARAMETERS</span></span>

### <span data-ttu-id="d3387-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3387-111">-DefaultProfile</span></span>
<span data-ttu-id="d3387-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3387-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3387-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3387-113">-ResourceGroupName</span></span>
<span data-ttu-id="d3387-114">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d3387-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3387-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="d3387-115">-RuleName</span></span>
<span data-ttu-id="d3387-116">Regel namn</span><span class="sxs-lookup"><span data-stu-id="d3387-116">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3387-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="d3387-117">-WebAppName</span></span>
<span data-ttu-id="d3387-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="d3387-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3387-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3387-119">-PassThru</span></span>
<span data-ttu-id="d3387-120">Returnera konfigurations objekt för åtkomst begränsning.</span><span class="sxs-lookup"><span data-stu-id="d3387-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="d3387-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d3387-121">-Confirm</span></span>
<span data-ttu-id="d3387-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d3387-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3387-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3387-123">-WhatIf</span></span>
<span data-ttu-id="d3387-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d3387-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3387-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d3387-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3387-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3387-126">CommonParameters</span></span>
<span data-ttu-id="d3387-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3387-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3387-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3387-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3387-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3387-129">INPUTS</span></span>

### <span data-ttu-id="d3387-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="d3387-130">None</span></span>

## <span data-ttu-id="d3387-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3387-131">OUTPUTS</span></span>

### <span data-ttu-id="d3387-132">Microsoft. Azure. Management. webbplatser. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="d3387-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="d3387-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3387-133">NOTES</span></span>

## <span data-ttu-id="d3387-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3387-134">RELATED LINKS</span></span>
[<span data-ttu-id="d3387-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d3387-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="d3387-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d3387-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="d3387-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="d3387-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)