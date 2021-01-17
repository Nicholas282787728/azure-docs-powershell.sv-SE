---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ded757d1e81ef5db94157f4676ed91dc11680fd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389973"
---
# <span data-ttu-id="2767a-101">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2767a-101">Remove-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="2767a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2767a-102">SYNOPSIS</span></span>
<span data-ttu-id="2767a-103">Tar bort SSL-profilen från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="2767a-103">Removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="2767a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2767a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2767a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2767a-105">DESCRIPTION</span></span>
<span data-ttu-id="2767a-106">Cmdleten **Remove-AzApplicationGatewaySslProfile** tar bort SSL-profilen från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="2767a-106">The **Remove-AzApplicationGatewaySslProfile** cmdlet removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="2767a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2767a-107">EXAMPLES</span></span>

### <span data-ttu-id="2767a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2767a-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

<span data-ttu-id="2767a-109">Det första kommandot får en Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="2767a-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="2767a-110">Det andra kommandot tar bort den SSL-profil som heter SslProfile01 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2767a-110">The second command removes the ssl profile named SslProfile01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2767a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2767a-111">PARAMETERS</span></span>

### <span data-ttu-id="2767a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2767a-112">-ApplicationGateway</span></span>
<span data-ttu-id="2767a-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2767a-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2767a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2767a-114">-DefaultProfile</span></span>
<span data-ttu-id="2767a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2767a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2767a-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="2767a-116">-Name</span></span>
<span data-ttu-id="2767a-117">Namnet på SSL-profilen</span><span class="sxs-lookup"><span data-stu-id="2767a-117">The name of the ssl profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2767a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2767a-118">CommonParameters</span></span>
<span data-ttu-id="2767a-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2767a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2767a-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2767a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2767a-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2767a-121">INPUTS</span></span>

### <span data-ttu-id="2767a-122">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2767a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2767a-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2767a-123">OUTPUTS</span></span>

### <span data-ttu-id="2767a-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2767a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2767a-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2767a-125">NOTES</span></span>

## <span data-ttu-id="2767a-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2767a-126">RELATED LINKS</span></span>

[<span data-ttu-id="2767a-127">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2767a-127">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="2767a-128">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2767a-128">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="2767a-129">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2767a-129">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="2767a-130">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2767a-130">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)