---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: b51aac195a6f0f4870b89894cce8f26c732077ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918298"
---
# <span data-ttu-id="c56a0-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="c56a0-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="c56a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c56a0-102">SYNOPSIS</span></span>
<span data-ttu-id="c56a0-103">Skapar en Azure-ExpressRoutePortIdentity.</span><span class="sxs-lookup"><span data-stu-id="c56a0-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="c56a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c56a0-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c56a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c56a0-105">DESCRIPTION</span></span>
<span data-ttu-id="c56a0-106">Cmdleten **New-AzExpressRoutePortIdentity** skapar ett lokalt Azure ExpressRoutePort-Identity-objekt.</span><span class="sxs-lookup"><span data-stu-id="c56a0-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="c56a0-107">Använd **New-AzExpressRoutePort** eller **set-AzExpressRoutePort** för att tilldela den till Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c56a0-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="c56a0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c56a0-108">EXAMPLES</span></span>

### <span data-ttu-id="c56a0-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c56a0-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="c56a0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c56a0-110">PARAMETERS</span></span>

### <span data-ttu-id="c56a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56a0-111">-DefaultProfile</span></span>
<span data-ttu-id="c56a0-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c56a0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c56a0-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="c56a0-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="c56a0-114">ResourceId för den användare tilldelade identiteten som ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c56a0-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="c56a0-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c56a0-115">-Confirm</span></span>
<span data-ttu-id="c56a0-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c56a0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c56a0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c56a0-117">-WhatIf</span></span>
<span data-ttu-id="c56a0-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c56a0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c56a0-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c56a0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c56a0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56a0-120">CommonParameters</span></span>
<span data-ttu-id="c56a0-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c56a0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56a0-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c56a0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56a0-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c56a0-123">INPUTS</span></span>

### <span data-ttu-id="c56a0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c56a0-124">System.String</span></span>

## <span data-ttu-id="c56a0-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c56a0-125">OUTPUTS</span></span>

### <span data-ttu-id="c56a0-126">Microsoft. Azure. commands. Networks. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="c56a0-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="c56a0-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c56a0-127">NOTES</span></span>

## <span data-ttu-id="c56a0-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c56a0-128">RELATED LINKS</span></span>
[<span data-ttu-id="c56a0-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="c56a0-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="c56a0-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="c56a0-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="c56a0-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="c56a0-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)