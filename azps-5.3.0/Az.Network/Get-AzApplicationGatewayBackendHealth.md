---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: 378c6ee91c438bfa70ab8e89e069ad81d3515e33
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522867"
---
# <span data-ttu-id="52166-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="52166-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="52166-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52166-102">SYNOPSIS</span></span>
<span data-ttu-id="52166-103">Hämtar Server delen för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="52166-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="52166-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52166-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52166-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52166-105">DESCRIPTION</span></span>
<span data-ttu-id="52166-106">Get-AzApplicationGatewayBackendHealth cmdlet får Server delen för Programgateway.</span><span class="sxs-lookup"><span data-stu-id="52166-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="52166-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52166-107">EXAMPLES</span></span>

### <span data-ttu-id="52166-108">Exempel 1: hämtar Server delen utan att utöka resurserna.</span><span class="sxs-lookup"><span data-stu-id="52166-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="52166-109">Det här kommandot hämtar Server delen för programgatewayen med namnet ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $BackendHealth variabel.</span><span class="sxs-lookup"><span data-stu-id="52166-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="52166-110">Exempel 2: hämtar Server delen med utökade resurser.</span><span class="sxs-lookup"><span data-stu-id="52166-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="52166-111">Det här kommandot hämtar Server delen (med utökad resurs) för programgatewayen med namnet ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $BackendHealth variabeln.</span><span class="sxs-lookup"><span data-stu-id="52166-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="52166-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52166-112">PARAMETERS</span></span>

### <span data-ttu-id="52166-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52166-113">-AsJob</span></span>
<span data-ttu-id="52166-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="52166-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52166-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52166-115">-DefaultProfile</span></span>
<span data-ttu-id="52166-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52166-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52166-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="52166-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52166-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="52166-118">-Name</span></span>
<span data-ttu-id="52166-119">Anger namnet på den Application Gateway som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="52166-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52166-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52166-120">-ResourceGroupName</span></span>
<span data-ttu-id="52166-121">Anger namnet på den resurs grupp som innehåller programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="52166-121">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52166-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52166-122">CommonParameters</span></span>
<span data-ttu-id="52166-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52166-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52166-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52166-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52166-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52166-125">INPUTS</span></span>

### <span data-ttu-id="52166-126">System. String</span><span class="sxs-lookup"><span data-stu-id="52166-126">System.String</span></span>

## <span data-ttu-id="52166-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52166-127">OUTPUTS</span></span>

### <span data-ttu-id="52166-128">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="52166-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="52166-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52166-129">NOTES</span></span>
<span data-ttu-id="52166-130">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="52166-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="52166-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52166-131">RELATED LINKS</span></span>

[<span data-ttu-id="52166-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="52166-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

