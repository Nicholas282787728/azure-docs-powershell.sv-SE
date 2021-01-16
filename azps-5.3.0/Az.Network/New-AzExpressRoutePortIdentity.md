---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421712"
---
# <span data-ttu-id="e1a7d-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e1a7d-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="e1a7d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a7d-103">Skapar en Azure-ExpressRoutePortIdentity.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="e1a7d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1a7d-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1a7d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1a7d-105">DESCRIPTION</span></span>
<span data-ttu-id="e1a7d-106">Cmdleten **New-AzExpressRoutePortIdentity** skapar ett lokalt Azure ExpressRoutePort-Identity-objekt.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="e1a7d-107">Använd **New-AzExpressRoutePort** eller **set-AzExpressRoutePort** för att tilldela den till Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="e1a7d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1a7d-108">EXAMPLES</span></span>

### <span data-ttu-id="e1a7d-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e1a7d-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="e1a7d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1a7d-110">PARAMETERS</span></span>

### <span data-ttu-id="e1a7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1a7d-111">-DefaultProfile</span></span>
<span data-ttu-id="e1a7d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1a7d-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="e1a7d-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="e1a7d-114">ResourceId för den användare tilldelade identiteten som ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a7d-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e1a7d-115">-Confirm</span></span>
<span data-ttu-id="e1a7d-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1a7d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1a7d-117">-WhatIf</span></span>
<span data-ttu-id="e1a7d-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1a7d-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1a7d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a7d-120">CommonParameters</span></span>
<span data-ttu-id="e1a7d-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1a7d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a7d-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1a7d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a7d-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1a7d-123">INPUTS</span></span>

### <span data-ttu-id="e1a7d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e1a7d-124">System.String</span></span>

## <span data-ttu-id="e1a7d-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1a7d-125">OUTPUTS</span></span>

### <span data-ttu-id="e1a7d-126">Microsoft. Azure. commands. Networks. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="e1a7d-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="e1a7d-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1a7d-127">NOTES</span></span>

## <span data-ttu-id="e1a7d-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1a7d-128">RELATED LINKS</span></span>
[<span data-ttu-id="e1a7d-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e1a7d-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="e1a7d-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e1a7d-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="e1a7d-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="e1a7d-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)