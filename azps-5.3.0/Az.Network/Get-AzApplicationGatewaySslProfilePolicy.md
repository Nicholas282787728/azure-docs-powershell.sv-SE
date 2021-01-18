---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: a1e6bd507b7ddcc0a70405136cb76bba9231a7f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522838"
---
# <span data-ttu-id="14f82-101">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="14f82-101">Get-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="14f82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14f82-102">SYNOPSIS</span></span>
<span data-ttu-id="14f82-103">Hämtar SSL-principen för en SSL-profil för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="14f82-103">Gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="14f82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14f82-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14f82-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14f82-105">DESCRIPTION</span></span>
<span data-ttu-id="14f82-106">Cmdleten **Get-AzApplicationGatewaySslProfilePolicy** hämtar SSL-principen för en SSL-profil för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="14f82-106">The **Get-AzApplicationGatewaySslProfilePolicy** cmdlet gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="14f82-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14f82-107">EXAMPLES</span></span>

### <span data-ttu-id="14f82-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="14f82-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

<span data-ttu-id="14f82-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="14f82-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="14f82-110">Det andra kommandot får den SSL-profil som heter SslProfile01 för $AppGw och lagrar den $SslProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="14f82-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="14f82-111">Med det senaste kommandot hämtas SSL-principen från SSL-profilen $SslProfile och lagras i $sslpolicy-variabeln.</span><span class="sxs-lookup"><span data-stu-id="14f82-111">The last command gets the SSL policy from the SSL profile $SslProfile and stores it in the $sslpolicy variable.</span></span>

## <span data-ttu-id="14f82-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14f82-112">PARAMETERS</span></span>

### <span data-ttu-id="14f82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f82-113">-DefaultProfile</span></span>
<span data-ttu-id="14f82-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14f82-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14f82-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="14f82-115">-SslProfile</span></span>
<span data-ttu-id="14f82-116">SSL-profilen för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="14f82-116">The application Gateway SSL profile</span></span>

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

### <span data-ttu-id="14f82-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f82-117">CommonParameters</span></span>
<span data-ttu-id="14f82-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14f82-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f82-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14f82-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f82-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14f82-120">INPUTS</span></span>

### <span data-ttu-id="14f82-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="14f82-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="14f82-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14f82-122">OUTPUTS</span></span>

### <span data-ttu-id="14f82-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="14f82-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="14f82-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14f82-124">NOTES</span></span>

## <span data-ttu-id="14f82-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14f82-125">RELATED LINKS</span></span>

[<span data-ttu-id="14f82-126">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="14f82-126">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="14f82-127">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="14f82-127">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="14f82-128">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="14f82-128">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="14f82-129">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="14f82-129">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)