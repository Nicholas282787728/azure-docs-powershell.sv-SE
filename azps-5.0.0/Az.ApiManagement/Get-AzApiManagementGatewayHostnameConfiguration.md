---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321940"
---
# <span data-ttu-id="d0ed5-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0ed5-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="d0ed5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="d0ed5-103">Hämtar all eller specifik värd konfiguration för den befintliga gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d0ed5-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="d0ed5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0ed5-104">SYNTAX</span></span>

### <span data-ttu-id="d0ed5-105">GetByGatewayId (standard)</span><span class="sxs-lookup"><span data-stu-id="d0ed5-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0ed5-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="d0ed5-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0ed5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0ed5-107">DESCRIPTION</span></span>
<span data-ttu-id="d0ed5-108">Cmdleten **Get-AzApiManagementGatewayHostnameConfiguration** hämtar all eller specifik värd konfiguration för den befintliga gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d0ed5-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="d0ed5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0ed5-109">EXAMPLES</span></span>

### <span data-ttu-id="d0ed5-110">Exempel 1: Hämta alla hostname-konfigurationer för gatewayen</span><span class="sxs-lookup"><span data-stu-id="d0ed5-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="d0ed5-111">Det här kommandot får alla hostname-konfigurationer för en "0123456789"-Gateway.</span><span class="sxs-lookup"><span data-stu-id="d0ed5-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="d0ed5-112">Exempel 2: skaffa en hostname-konfiguration för gatewayen</span><span class="sxs-lookup"><span data-stu-id="d0ed5-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="d0ed5-113">Med det här kommandot får du "123"-värd konfiguration för en "0123456789"-Gateway.</span><span class="sxs-lookup"><span data-stu-id="d0ed5-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="d0ed5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0ed5-114">PARAMETERS</span></span>

### <span data-ttu-id="d0ed5-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d0ed5-115">-Context</span></span>
<span data-ttu-id="d0ed5-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d0ed5-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d0ed5-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d0ed5-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0ed5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0ed5-118">-DefaultProfile</span></span>
<span data-ttu-id="d0ed5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ed5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0ed5-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d0ed5-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="d0ed5-121">Konfigurations identifierare för hostname.</span><span class="sxs-lookup"><span data-stu-id="d0ed5-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="d0ed5-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d0ed5-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayHostnameId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0ed5-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="d0ed5-123">-GatewayId</span></span>
<span data-ttu-id="d0ed5-124">Gateway-ID.</span><span class="sxs-lookup"><span data-stu-id="d0ed5-124">Gateway identifier.</span></span>
<span data-ttu-id="d0ed5-125">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d0ed5-125">This parameter is required.</span></span>

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

### <span data-ttu-id="d0ed5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0ed5-126">CommonParameters</span></span>
<span data-ttu-id="d0ed5-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0ed5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0ed5-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0ed5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0ed5-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0ed5-129">INPUTS</span></span>

### <span data-ttu-id="d0ed5-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d0ed5-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d0ed5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d0ed5-131">System.String</span></span>

## <span data-ttu-id="d0ed5-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0ed5-132">OUTPUTS</span></span>

### <span data-ttu-id="d0ed5-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0ed5-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="d0ed5-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0ed5-134">NOTES</span></span>

## <span data-ttu-id="d0ed5-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0ed5-135">RELATED LINKS</span></span>
