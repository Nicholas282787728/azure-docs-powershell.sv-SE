---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403088"
---
# <span data-ttu-id="16e4c-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="16e4c-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="16e4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="16e4c-103">Skapar en Azure-ExpressRoutePortIdentity.</span><span class="sxs-lookup"><span data-stu-id="16e4c-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="16e4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16e4c-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16e4c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16e4c-105">DESCRIPTION</span></span>
<span data-ttu-id="16e4c-106">Cmdleten **New-AzExpressRoutePortIdentity** skapar ett lokalt Azure ExpressRoutePort-Identity-objekt.</span><span class="sxs-lookup"><span data-stu-id="16e4c-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="16e4c-107">Använd **New-AzExpressRoutePort** eller **set-AzExpressRoutePort** för att tilldela den till Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="16e4c-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="16e4c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16e4c-108">EXAMPLES</span></span>

### <span data-ttu-id="16e4c-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="16e4c-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="16e4c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16e4c-110">PARAMETERS</span></span>

### <span data-ttu-id="16e4c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e4c-111">-DefaultProfile</span></span>
<span data-ttu-id="16e4c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16e4c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16e4c-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="16e4c-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="16e4c-114">ResourceId för den användare tilldelade identiteten som ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="16e4c-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="16e4c-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="16e4c-115">-Confirm</span></span>
<span data-ttu-id="16e4c-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="16e4c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e4c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e4c-117">-WhatIf</span></span>
<span data-ttu-id="16e4c-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="16e4c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16e4c-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="16e4c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e4c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e4c-120">CommonParameters</span></span>
<span data-ttu-id="16e4c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e4c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e4c-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e4c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e4c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16e4c-123">INPUTS</span></span>

### <span data-ttu-id="16e4c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="16e4c-124">System.String</span></span>

## <span data-ttu-id="16e4c-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16e4c-125">OUTPUTS</span></span>

### <span data-ttu-id="16e4c-126">Microsoft. Azure. commands. Networks. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="16e4c-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="16e4c-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16e4c-127">NOTES</span></span>

## <span data-ttu-id="16e4c-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16e4c-128">RELATED LINKS</span></span>
[<span data-ttu-id="16e4c-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="16e4c-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="16e4c-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="16e4c-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="16e4c-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="16e4c-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)