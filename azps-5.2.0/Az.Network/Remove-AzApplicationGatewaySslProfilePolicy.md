---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 541293160a1cf9e3d32de5d378c24d1ee4b2705b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389970"
---
# <span data-ttu-id="5a84a-101">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5a84a-101">Remove-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="5a84a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a84a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a84a-103">Tar bort en SSL-princip från en Azure Application Gateway SSL-profil.</span><span class="sxs-lookup"><span data-stu-id="5a84a-103">Removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="5a84a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a84a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a84a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a84a-105">DESCRIPTION</span></span>
<span data-ttu-id="5a84a-106">Remove-AzApplicationGatewaySslProfilePolicy cmdlet tar bort en SSL-princip från en Azure Application Gateway SSL-profil.</span><span class="sxs-lookup"><span data-stu-id="5a84a-106">The Remove-AzApplicationGatewaySslProfilePolicy cmdlet removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="5a84a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a84a-107">EXAMPLES</span></span>

### <span data-ttu-id="5a84a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5a84a-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> $profile = Remove-AzApplicationGatewaySslProfilePolicy -SslProfile $profile
```

<span data-ttu-id="5a84a-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="5a84a-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="5a84a-110">Det andra kommandot får den SSL-profil som heter Profile01 för $AppGw och lagrar den i $profile-variabeln.</span><span class="sxs-lookup"><span data-stu-id="5a84a-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="5a84a-111">Det senaste kommandot tar bort SSL-principen för SSL-profilen som lagras i $profile.</span><span class="sxs-lookup"><span data-stu-id="5a84a-111">The last command removes the ssl policy of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="5a84a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a84a-112">PARAMETERS</span></span>

### <span data-ttu-id="5a84a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a84a-113">-DefaultProfile</span></span>
<span data-ttu-id="5a84a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a84a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a84a-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="5a84a-115">-SslProfile</span></span>
<span data-ttu-id="5a84a-116">ApplicationGateway SSL-profil</span><span class="sxs-lookup"><span data-stu-id="5a84a-116">The applicationGateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a84a-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5a84a-117">-Confirm</span></span>
<span data-ttu-id="5a84a-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5a84a-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a84a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a84a-119">-WhatIf</span></span>
<span data-ttu-id="5a84a-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5a84a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a84a-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5a84a-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a84a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a84a-122">CommonParameters</span></span>
<span data-ttu-id="5a84a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a84a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a84a-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a84a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a84a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a84a-125">INPUTS</span></span>

### <span data-ttu-id="5a84a-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5a84a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="5a84a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a84a-127">OUTPUTS</span></span>

### <span data-ttu-id="5a84a-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5a84a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="5a84a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a84a-129">NOTES</span></span>

## <span data-ttu-id="5a84a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a84a-130">RELATED LINKS</span></span>

[<span data-ttu-id="5a84a-131">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5a84a-131">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="5a84a-132">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5a84a-132">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="5a84a-133">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5a84a-133">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="5a84a-134">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="5a84a-134">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)