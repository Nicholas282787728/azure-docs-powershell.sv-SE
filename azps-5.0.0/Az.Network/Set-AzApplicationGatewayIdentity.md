---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: aa21ea0719c36e5b737b478657e0734eb21a3c3f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325230"
---
# <span data-ttu-id="8b143-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="8b143-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="8b143-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b143-102">SYNOPSIS</span></span>
<span data-ttu-id="8b143-103">Uppdaterar en identitet som tilldelats programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="8b143-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="8b143-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b143-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b143-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b143-105">DESCRIPTION</span></span>
<span data-ttu-id="8b143-106">Cmdleten **set-AzApplicationGatewayIdentity** uppdaterar en identitet som tilldelats till Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8b143-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="8b143-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b143-107">EXAMPLES</span></span>

### <span data-ttu-id="8b143-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8b143-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="8b143-109">I det här exemplet tilldelar vi en användare tilldelad identitet till en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8b143-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="8b143-110">OBS! den här identiteten bör ha åtkomst till det valv som certifikat/hemligheter refererar till.</span><span class="sxs-lookup"><span data-stu-id="8b143-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="8b143-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b143-111">PARAMETERS</span></span>

### <span data-ttu-id="8b143-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b143-112">-ApplicationGateway</span></span>
<span data-ttu-id="8b143-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b143-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b143-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b143-114">-DefaultProfile</span></span>
<span data-ttu-id="8b143-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b143-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b143-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="8b143-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="8b143-117">ResourceId för den användare tilldelade identiteten som ska kopplas till programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="8b143-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="8b143-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8b143-118">-Confirm</span></span>
<span data-ttu-id="8b143-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8b143-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b143-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b143-120">-WhatIf</span></span>
<span data-ttu-id="8b143-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8b143-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b143-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8b143-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b143-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b143-123">CommonParameters</span></span>
<span data-ttu-id="8b143-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b143-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b143-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b143-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b143-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b143-126">INPUTS</span></span>

### <span data-ttu-id="8b143-127">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b143-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="8b143-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8b143-128">System.String</span></span>

## <span data-ttu-id="8b143-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b143-129">OUTPUTS</span></span>

### <span data-ttu-id="8b143-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b143-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8b143-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b143-131">NOTES</span></span>

## <span data-ttu-id="8b143-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b143-132">RELATED LINKS</span></span>