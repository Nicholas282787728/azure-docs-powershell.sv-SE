---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388689"
---
# <span data-ttu-id="d1d53-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="d1d53-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="d1d53-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1d53-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d53-103">Hämtar alla eller specifika API-hanterings-Gateway.</span><span class="sxs-lookup"><span data-stu-id="d1d53-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="d1d53-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1d53-104">SYNTAX</span></span>

### <span data-ttu-id="d1d53-105">GetAllGateways (standard)</span><span class="sxs-lookup"><span data-stu-id="d1d53-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1d53-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="d1d53-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1d53-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1d53-107">DESCRIPTION</span></span>
<span data-ttu-id="d1d53-108">Cmdleten **Get-AzApiManagementGateway** hämtar alla eller specifika API-hanterings-Gateway.</span><span class="sxs-lookup"><span data-stu-id="d1d53-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="d1d53-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1d53-109">EXAMPLES</span></span>

### <span data-ttu-id="d1d53-110">Exempel 1: Hämta alla gateways</span><span class="sxs-lookup"><span data-stu-id="d1d53-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="d1d53-111">Det här kommandot får alla gateways.</span><span class="sxs-lookup"><span data-stu-id="d1d53-111">This command gets all gateways.</span></span>

### <span data-ttu-id="d1d53-112">Exempel 2: skaffa en gateway utifrån ID</span><span class="sxs-lookup"><span data-stu-id="d1d53-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="d1d53-113">Det här kommandot får Gateway 0123456789.</span><span class="sxs-lookup"><span data-stu-id="d1d53-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="d1d53-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1d53-114">PARAMETERS</span></span>

### <span data-ttu-id="d1d53-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d1d53-115">-Context</span></span>
<span data-ttu-id="d1d53-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d1d53-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d1d53-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d1d53-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d53-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d53-118">-DefaultProfile</span></span>
<span data-ttu-id="d1d53-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1d53-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1d53-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="d1d53-120">-GatewayId</span></span>
<span data-ttu-id="d1d53-121">Identifierare för en gateway.</span><span class="sxs-lookup"><span data-stu-id="d1d53-121">Identifier of a gateway.</span></span>
<span data-ttu-id="d1d53-122">Om det här alternativet anges kommer gatewayen att hittas.</span><span class="sxs-lookup"><span data-stu-id="d1d53-122">If specified will try to find gateway by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d53-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d53-123">CommonParameters</span></span>
<span data-ttu-id="d1d53-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1d53-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d53-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1d53-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d53-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1d53-126">INPUTS</span></span>

### <span data-ttu-id="d1d53-127">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d1d53-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d1d53-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d1d53-128">System.String</span></span>

## <span data-ttu-id="d1d53-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1d53-129">OUTPUTS</span></span>

### <span data-ttu-id="d1d53-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="d1d53-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="d1d53-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1d53-131">NOTES</span></span>

## <span data-ttu-id="d1d53-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1d53-132">RELATED LINKS</span></span>
