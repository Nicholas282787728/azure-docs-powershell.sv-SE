---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393360"
---
# <span data-ttu-id="54f12-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="54f12-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="54f12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54f12-102">SYNOPSIS</span></span>
<span data-ttu-id="54f12-103">Skapar en IP-konfiguration som associeras med PrivateLink-konfigurationen</span><span class="sxs-lookup"><span data-stu-id="54f12-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="54f12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54f12-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54f12-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54f12-105">DESCRIPTION</span></span>
<span data-ttu-id="54f12-106">Cmdleten **New-AzApplicationGatewayPrivateLinkIpConfiguration** skapar en IP-konfiguration som associeras med PrivateLink-konfigurationen för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="54f12-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="54f12-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54f12-107">EXAMPLES</span></span>

### <span data-ttu-id="54f12-108">Exempel 1: PrivateLink IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="54f12-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="54f12-109">Det här kommandot skapar en PrivateLink IP-konfiguration med namnet "ipConfig01" lagrar resultatet i variabeln som heter $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="54f12-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="54f12-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54f12-110">PARAMETERS</span></span>

### <span data-ttu-id="54f12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f12-111">-DefaultProfile</span></span>
<span data-ttu-id="54f12-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54f12-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54f12-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="54f12-113">-Name</span></span>
<span data-ttu-id="54f12-114">Namnet på IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="54f12-114">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="54f12-115">-Primär</span><span class="sxs-lookup"><span data-stu-id="54f12-115">-Primary</span></span>
<span data-ttu-id="54f12-116">Ange att IP-konfigurationen är primär.</span><span class="sxs-lookup"><span data-stu-id="54f12-116">Indicate the ip configuration is primary.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f12-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="54f12-117">-PrivateIpAddress</span></span>
<span data-ttu-id="54f12-118">Den privata IP-adressen för ipConfiguration om statisk tilldelning önskas.</span><span class="sxs-lookup"><span data-stu-id="54f12-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="54f12-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="54f12-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="54f12-120">IP-version för IP-konfigurationen</span><span class="sxs-lookup"><span data-stu-id="54f12-120">The ip version of the ip configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f12-121">-Undernät</span><span class="sxs-lookup"><span data-stu-id="54f12-121">-Subnet</span></span>
<span data-ttu-id="54f12-122">Under</span><span class="sxs-lookup"><span data-stu-id="54f12-122">Subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f12-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f12-123">CommonParameters</span></span>
<span data-ttu-id="54f12-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54f12-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f12-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54f12-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f12-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54f12-126">INPUTS</span></span>

### <span data-ttu-id="54f12-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="54f12-127">None</span></span>

## <span data-ttu-id="54f12-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54f12-128">OUTPUTS</span></span>

### <span data-ttu-id="54f12-129">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="54f12-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="54f12-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54f12-130">NOTES</span></span>

## <span data-ttu-id="54f12-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54f12-131">RELATED LINKS</span></span>

[<span data-ttu-id="54f12-132">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="54f12-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
