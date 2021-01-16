---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 6d4bab8f7c4c766730dd6fb09f0d0a011d5d3739
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396368"
---
# <span data-ttu-id="866b1-101">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="866b1-101">Get-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="866b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="866b1-102">SYNOPSIS</span></span>
<span data-ttu-id="866b1-103">Hämtar SSL-profilen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="866b1-103">Gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="866b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="866b1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="866b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="866b1-105">DESCRIPTION</span></span>
<span data-ttu-id="866b1-106">Cmdleten **Get-AzApplicationGatewaySslProfile** hämtar SSL-profilen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="866b1-106">The **Get-AzApplicationGatewaySslProfile** cmdlet gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="866b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="866b1-107">EXAMPLES</span></span>

### <span data-ttu-id="866b1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="866b1-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

<span data-ttu-id="866b1-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot hämtar SSL-SslProfile01 för $AppGw och lagrar den i $profile-variabeln.</span><span class="sxs-lookup"><span data-stu-id="866b1-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the SSL profile SslProfile01 for $AppGw and stores it in the $profile variable.</span></span>

## <span data-ttu-id="866b1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="866b1-110">PARAMETERS</span></span>

### <span data-ttu-id="866b1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="866b1-111">-ApplicationGateway</span></span>
<span data-ttu-id="866b1-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="866b1-112">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="866b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866b1-113">-DefaultProfile</span></span>
<span data-ttu-id="866b1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="866b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="866b1-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="866b1-115">-Name</span></span>
<span data-ttu-id="866b1-116">Namnet på SSL-profilen</span><span class="sxs-lookup"><span data-stu-id="866b1-116">The name of the ssl profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="866b1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866b1-117">CommonParameters</span></span>
<span data-ttu-id="866b1-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="866b1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866b1-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="866b1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866b1-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="866b1-120">INPUTS</span></span>

### <span data-ttu-id="866b1-121">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="866b1-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="866b1-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="866b1-122">OUTPUTS</span></span>

### <span data-ttu-id="866b1-123">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="866b1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="866b1-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="866b1-124">NOTES</span></span>

## <span data-ttu-id="866b1-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="866b1-125">RELATED LINKS</span></span>

[<span data-ttu-id="866b1-126">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="866b1-126">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="866b1-127">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="866b1-127">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="866b1-128">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="866b1-128">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="866b1-129">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="866b1-129">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)