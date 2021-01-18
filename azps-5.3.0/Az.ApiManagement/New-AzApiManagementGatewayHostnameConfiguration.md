---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525026"
---
# <span data-ttu-id="3d6e1-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d6e1-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="3d6e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6e1-103">Skapar en hostname-configuratin för den befintliga gatewayen.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="3d6e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d6e1-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d6e1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d6e1-105">DESCRIPTION</span></span>
<span data-ttu-id="3d6e1-106">Cmdleten **New-AzApiManagementGatewayHostnameConfiguration** skapar ett värdnamn configuratin för den befintliga gatewayen.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="3d6e1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d6e1-107">EXAMPLES</span></span>

### <span data-ttu-id="3d6e1-108">Exempel 1: skapa en hostname-konfiguration för den befintliga gatewayen</span><span class="sxs-lookup"><span data-stu-id="3d6e1-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="3d6e1-109">Det här kommandot skapar en "h01"-konfiguration för en "G01"-Gateway.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="3d6e1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d6e1-110">PARAMETERS</span></span>

### <span data-ttu-id="3d6e1-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="3d6e1-111">-CertificateResourceId</span></span>
<span data-ttu-id="3d6e1-112">En resurs-ID för det befintliga certifikat-ID: t. Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="3d6e1-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3d6e1-113">-Context</span></span>
<span data-ttu-id="3d6e1-114">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3d6e1-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-115">This parameter is required.</span></span>

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

### <span data-ttu-id="3d6e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d6e1-116">-DefaultProfile</span></span>
<span data-ttu-id="3d6e1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d6e1-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3d6e1-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="3d6e1-119">ID för ny Gateway-värdnamn confiuration.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="3d6e1-120">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-120">This parameter is optional.</span></span>
<span data-ttu-id="3d6e1-121">Om det inte anges kommer att genereras.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-121">If not specified will be generated.</span></span>

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

### <span data-ttu-id="3d6e1-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3d6e1-122">-GatewayId</span></span>
<span data-ttu-id="3d6e1-123">Identifierare för befintlig gateway.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="3d6e1-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-124">This parameter is required.</span></span>

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

### <span data-ttu-id="3d6e1-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="3d6e1-125">-Hostname</span></span>
<span data-ttu-id="3d6e1-126">Namn.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-126">Hostname.</span></span>
<span data-ttu-id="3d6e1-127">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-127">This parameter is required.</span></span>

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

### <span data-ttu-id="3d6e1-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3d6e1-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="3d6e1-129">Flagga för att tvinga NegotiateClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="3d6e1-130">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-130">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6e1-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d6e1-131">-Confirm</span></span>
<span data-ttu-id="3d6e1-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d6e1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d6e1-133">-WhatIf</span></span>
<span data-ttu-id="3d6e1-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d6e1-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d6e1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6e1-136">CommonParameters</span></span>
<span data-ttu-id="3d6e1-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d6e1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6e1-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d6e1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6e1-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d6e1-139">INPUTS</span></span>

### <span data-ttu-id="3d6e1-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3d6e1-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3d6e1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3d6e1-141">System.String</span></span>

### <span data-ttu-id="3d6e1-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3d6e1-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3d6e1-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d6e1-143">OUTPUTS</span></span>

### <span data-ttu-id="3d6e1-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d6e1-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="3d6e1-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d6e1-145">NOTES</span></span>

## <span data-ttu-id="3d6e1-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d6e1-146">RELATED LINKS</span></span>
