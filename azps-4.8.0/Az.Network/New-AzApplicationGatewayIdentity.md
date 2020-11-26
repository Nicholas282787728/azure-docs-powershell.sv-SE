---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260751"
---
# <span data-ttu-id="7e1a4-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="7e1a4-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="7e1a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e1a4-102">SYNOPSIS</span></span>
<span data-ttu-id="7e1a4-103">Skapar ett identitets objekt för en programport.</span><span class="sxs-lookup"><span data-stu-id="7e1a4-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="7e1a4-104">Detta refererar till den användare som tilldelats identiteten.</span><span class="sxs-lookup"><span data-stu-id="7e1a4-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="7e1a4-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e1a4-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e1a4-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e1a4-106">DESCRIPTION</span></span>
<span data-ttu-id="7e1a4-107">**New-AzApplicationGatewayIdentity** cmdlet skapar ett Identity-objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7e1a4-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="7e1a4-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e1a4-108">EXAMPLES</span></span>

### <span data-ttu-id="7e1a4-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7e1a4-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="7e1a4-110">I det här exemplet skapar vi en användare tilldelad identitet och refererar den sedan till Identity-objekt som används med Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7e1a4-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="7e1a4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e1a4-111">PARAMETERS</span></span>

### <span data-ttu-id="7e1a4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e1a4-112">-DefaultProfile</span></span>
<span data-ttu-id="7e1a4-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e1a4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e1a4-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="7e1a4-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="7e1a4-115">ResourceId för den användare tilldelade identiteten som ska kopplas till programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="7e1a4-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="7e1a4-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7e1a4-116">-Confirm</span></span>
<span data-ttu-id="7e1a4-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7e1a4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e1a4-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e1a4-118">-WhatIf</span></span>
<span data-ttu-id="7e1a4-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7e1a4-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e1a4-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7e1a4-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e1a4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e1a4-121">CommonParameters</span></span>
<span data-ttu-id="7e1a4-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e1a4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e1a4-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e1a4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e1a4-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e1a4-124">INPUTS</span></span>

### <span data-ttu-id="7e1a4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7e1a4-125">System.String</span></span>

## <span data-ttu-id="7e1a4-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e1a4-126">OUTPUTS</span></span>

### <span data-ttu-id="7e1a4-127">Microsoft. Azure. commands. Networks. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="7e1a4-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="7e1a4-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e1a4-128">NOTES</span></span>

## <span data-ttu-id="7e1a4-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e1a4-129">RELATED LINKS</span></span>