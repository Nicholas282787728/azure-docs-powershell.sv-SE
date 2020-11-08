---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091310"
---
# <span data-ttu-id="bbe5b-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="bbe5b-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="bbe5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bbe5b-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe5b-103">Hämta de servervariabler som stöds och tillgängliga begäran och svars rubriker.</span><span class="sxs-lookup"><span data-stu-id="bbe5b-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="bbe5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bbe5b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="bbe5b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bbe5b-105">DESCRIPTION</span></span>
<span data-ttu-id="bbe5b-106">Cmdleten **Get-AzApplicationGatewayAvailableServerVariableAndHeader** hämtar de servervariabler som stöds och tillgängliga begäran och svars rubriker.</span><span class="sxs-lookup"><span data-stu-id="bbe5b-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="bbe5b-107">Parametrar kan användas för att hämta variabel-och rubrik listorna.</span><span class="sxs-lookup"><span data-stu-id="bbe5b-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="bbe5b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bbe5b-108">EXAMPLES</span></span>

### <span data-ttu-id="bbe5b-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bbe5b-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="bbe5b-110">De här kommandona returnerar alla tillgängliga servervariabler.</span><span class="sxs-lookup"><span data-stu-id="bbe5b-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="bbe5b-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bbe5b-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="bbe5b-112">Det här kommandot returnerar alla tillgängliga begärandehuvuden.</span><span class="sxs-lookup"><span data-stu-id="bbe5b-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="bbe5b-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="bbe5b-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="bbe5b-114">Det här kommandot returnerar alla tillgängliga svars rubriker.</span><span class="sxs-lookup"><span data-stu-id="bbe5b-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="bbe5b-115">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="bbe5b-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="bbe5b-116">De här kommandona returnerar alla tillgängliga servervariabler, Request och Response-rubriker.</span><span class="sxs-lookup"><span data-stu-id="bbe5b-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="bbe5b-117">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="bbe5b-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="bbe5b-118">De här kommandona returnerar alla tillgängliga servervariabler, Request och Response-rubriker.</span><span class="sxs-lookup"><span data-stu-id="bbe5b-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="bbe5b-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bbe5b-119">PARAMETERS</span></span>

### <span data-ttu-id="bbe5b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe5b-120">-DefaultProfile</span></span>
<span data-ttu-id="bbe5b-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bbe5b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbe5b-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="bbe5b-122">-RequestHeader</span></span>
<span data-ttu-id="bbe5b-123">Tillgängliga begärandehuvuden för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="bbe5b-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="bbe5b-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="bbe5b-124">-ResponseHeader</span></span>
<span data-ttu-id="bbe5b-125">Tillgängliga svars rubriker för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="bbe5b-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="bbe5b-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="bbe5b-126">-ServerVariable</span></span>
<span data-ttu-id="bbe5b-127">Tillgängliga servervariabler för programgateways.</span><span class="sxs-lookup"><span data-stu-id="bbe5b-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="bbe5b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe5b-128">CommonParameters</span></span>
<span data-ttu-id="bbe5b-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbe5b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe5b-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbe5b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe5b-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bbe5b-131">INPUTS</span></span>

### <span data-ttu-id="bbe5b-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="bbe5b-132">None</span></span>

## <span data-ttu-id="bbe5b-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bbe5b-133">OUTPUTS</span></span>

### <span data-ttu-id="bbe5b-134">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="bbe5b-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="bbe5b-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bbe5b-135">NOTES</span></span>
<span data-ttu-id="bbe5b-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** är ett alias för cmdleten **Get-AzApplicationGatewayAvailableServerVariableAndHeader** .</span><span class="sxs-lookup"><span data-stu-id="bbe5b-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="bbe5b-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bbe5b-137">RELATED LINKS</span></span>
