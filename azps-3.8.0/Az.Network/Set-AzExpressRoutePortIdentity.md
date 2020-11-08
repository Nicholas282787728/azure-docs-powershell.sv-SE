---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: af04f3540aaf0ec90432c3b1262b45ef9ef1c2cd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089060"
---
# <span data-ttu-id="513e0-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="513e0-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="513e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="513e0-102">SYNOPSIS</span></span>
<span data-ttu-id="513e0-103">Uppdaterar en identitet som tilldelats till en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="513e0-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="513e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="513e0-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="513e0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="513e0-105">DESCRIPTION</span></span>
<span data-ttu-id="513e0-106">Cmdleten **set-AzExpressRoutePortIdentity** uppdaterar ett lokalt Azure ExpressRoutePort-objekt.</span><span class="sxs-lookup"><span data-stu-id="513e0-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="513e0-107">Använd **set-AzExpressRoutePort** för att tilldela den till ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="513e0-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="513e0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="513e0-108">EXAMPLES</span></span>

### <span data-ttu-id="513e0-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="513e0-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="513e0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="513e0-110">PARAMETERS</span></span>

### <span data-ttu-id="513e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513e0-111">-DefaultProfile</span></span>
<span data-ttu-id="513e0-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="513e0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="513e0-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="513e0-113">-ExpressRoutePort</span></span>
<span data-ttu-id="513e0-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="513e0-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="513e0-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="513e0-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="513e0-116">ResourceId för den användare tilldelade identiteten som ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="513e0-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="513e0-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="513e0-117">-Confirm</span></span>
<span data-ttu-id="513e0-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="513e0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="513e0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="513e0-119">-WhatIf</span></span>
<span data-ttu-id="513e0-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="513e0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="513e0-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="513e0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="513e0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513e0-122">CommonParameters</span></span>
<span data-ttu-id="513e0-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="513e0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513e0-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="513e0-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513e0-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="513e0-125">INPUTS</span></span>

### <span data-ttu-id="513e0-126">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="513e0-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="513e0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="513e0-127">System.String</span></span>

## <span data-ttu-id="513e0-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="513e0-128">OUTPUTS</span></span>

### <span data-ttu-id="513e0-129">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="513e0-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="513e0-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="513e0-130">NOTES</span></span>

## <span data-ttu-id="513e0-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="513e0-131">RELATED LINKS</span></span>
[<span data-ttu-id="513e0-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="513e0-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="513e0-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="513e0-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="513e0-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="513e0-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)