---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
ms.openlocfilehash: 925e4949b444c9338fad3f88cf5066430e1b5a75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575378"
---
# <span data-ttu-id="8652c-101">New-AzureRmApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8652c-101">New-AzureRmApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="8652c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8652c-102">SYNOPSIS</span></span>
<span data-ttu-id="8652c-103">Skapar ett objekt av `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="8652c-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8652c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8652c-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint <String[]>
 -ClientCertificateThumbprint <String> [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>]
 [-ServerCertificateThumbprint <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8652c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8652c-105">DESCRIPTION</span></span>

<span data-ttu-id="8652c-106">Cmdleten **New-AzureRmApiManagementBackendServiceFabric** skapar ett objekt som `PsApiManagementServiceFabric` ska användas i cmdlet **New-AzureRmApiManagementBackend** och **set-AzureRmApiManagementBackend**.</span><span class="sxs-lookup"><span data-stu-id="8652c-106">The **New-AzureRmApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzureRmApiManagementBackend** and **Set-AzureRmApiManagementBackend**.</span></span>

## <span data-ttu-id="8652c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8652c-107">EXAMPLES</span></span>

### <span data-ttu-id="8652c-108">Exempel 1: skapa ett In-Memory objekt för backend-tjänsten</span><span class="sxs-lookup"><span data-stu-id="8652c-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="8652c-109">Skapar ett infrastruktur avtal för en server dels tjänst</span><span class="sxs-lookup"><span data-stu-id="8652c-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="8652c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8652c-110">PARAMETERS</span></span>

### <span data-ttu-id="8652c-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="8652c-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="8652c-112">Tumavtryck för klient certifikat för hanterings slut punkten.</span><span class="sxs-lookup"><span data-stu-id="8652c-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="8652c-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="8652c-113">This parameter is required.</span></span>

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

### <span data-ttu-id="8652c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8652c-114">-DefaultProfile</span></span>
<span data-ttu-id="8652c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8652c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8652c-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="8652c-116">-ManagementEndpoint</span></span>
<span data-ttu-id="8652c-117">Slut punkter för hantering av Service Fabric-kluster.</span><span class="sxs-lookup"><span data-stu-id="8652c-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="8652c-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="8652c-118">This parameter is required.</span></span>

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

### <span data-ttu-id="8652c-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="8652c-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="8652c-120">Maximalt antal försök när du löser en tjänst infrastruktur partition.</span><span class="sxs-lookup"><span data-stu-id="8652c-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="8652c-121">Denna parameter är valfri och standardvärdet är 5.</span><span class="sxs-lookup"><span data-stu-id="8652c-121">This parameter is optional and default value is 5.</span></span>

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

### <span data-ttu-id="8652c-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="8652c-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="8652c-123">Tumavtryck för certifikat kluster hanterings tjänsten används för TLS-kommunikation. Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="8652c-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="8652c-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="8652c-124">-ServerX509Name</span></span>
<span data-ttu-id="8652c-125">Insamling av Server X509-certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="8652c-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="8652c-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="8652c-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="8652c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8652c-127">CommonParameters</span></span>
<span data-ttu-id="8652c-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8652c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8652c-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8652c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8652c-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8652c-130">INPUTS</span></span>

### <span data-ttu-id="8652c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8652c-131">System.String</span></span>

## <span data-ttu-id="8652c-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8652c-132">OUTPUTS</span></span>

### <span data-ttu-id="8652c-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8652c-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="8652c-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8652c-134">NOTES</span></span>

## <span data-ttu-id="8652c-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8652c-135">RELATED LINKS</span></span>

[<span data-ttu-id="8652c-136">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8652c-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="8652c-137">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8652c-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="8652c-138">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8652c-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="8652c-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8652c-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="8652c-140">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8652c-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
