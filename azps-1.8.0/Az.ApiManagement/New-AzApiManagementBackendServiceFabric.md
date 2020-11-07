---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 193f8f64abee3514d94a0f825beb7190c8ea7fa6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743366"
---
# <span data-ttu-id="388bc-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="388bc-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="388bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="388bc-102">SYNOPSIS</span></span>
<span data-ttu-id="388bc-103">Skapar ett objekt av `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="388bc-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="388bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="388bc-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="388bc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="388bc-105">DESCRIPTION</span></span>

<span data-ttu-id="388bc-106">Cmdleten **New-AzApiManagementBackendServiceFabric** skapar ett objekt som `PsApiManagementServiceFabric` ska användas i cmdlet **New-AzApiManagementBackend** och **set-AzApiManagementBackend**.</span><span class="sxs-lookup"><span data-stu-id="388bc-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="388bc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="388bc-107">EXAMPLES</span></span>

### <span data-ttu-id="388bc-108">Exempel 1: skapa ett In-Memory objekt för backend-tjänsten</span><span class="sxs-lookup"><span data-stu-id="388bc-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="388bc-109">Skapar ett infrastruktur avtal för en server dels tjänst</span><span class="sxs-lookup"><span data-stu-id="388bc-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="388bc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="388bc-110">PARAMETERS</span></span>

### <span data-ttu-id="388bc-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="388bc-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="388bc-112">Tumavtryck för klient certifikat för hanterings slut punkten.</span><span class="sxs-lookup"><span data-stu-id="388bc-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="388bc-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="388bc-113">This parameter is required.</span></span>

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

### <span data-ttu-id="388bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="388bc-114">-DefaultProfile</span></span>
<span data-ttu-id="388bc-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="388bc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="388bc-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="388bc-116">-ManagementEndpoint</span></span>
<span data-ttu-id="388bc-117">Slut punkter för hantering av Service Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="388bc-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="388bc-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="388bc-118">This parameter is required.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="388bc-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="388bc-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="388bc-120">Maximalt antal försök när du löser en tjänst infrastruktur partition.</span><span class="sxs-lookup"><span data-stu-id="388bc-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="388bc-121">Denna parameter är valfri och standardvärdet är 5.</span><span class="sxs-lookup"><span data-stu-id="388bc-121">This parameter is optional and default value is 5.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="388bc-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="388bc-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="388bc-123">Tumavtryck för certifikat kluster hanterings tjänsten används för TLS-kommunikation. Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="388bc-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="388bc-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="388bc-124">-ServerX509Name</span></span>
<span data-ttu-id="388bc-125">Insamling av Server X509-certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="388bc-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="388bc-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="388bc-126">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="388bc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388bc-127">CommonParameters</span></span>
<span data-ttu-id="388bc-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="388bc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388bc-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="388bc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388bc-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="388bc-130">INPUTS</span></span>

### <span data-ttu-id="388bc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="388bc-131">System.String</span></span>

## <span data-ttu-id="388bc-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="388bc-132">OUTPUTS</span></span>

### <span data-ttu-id="388bc-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="388bc-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="388bc-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="388bc-134">NOTES</span></span>

## <span data-ttu-id="388bc-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="388bc-135">RELATED LINKS</span></span>

[<span data-ttu-id="388bc-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="388bc-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="388bc-137">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="388bc-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="388bc-138">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="388bc-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="388bc-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="388bc-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="388bc-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="388bc-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
