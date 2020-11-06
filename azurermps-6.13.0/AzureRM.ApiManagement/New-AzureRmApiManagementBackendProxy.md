---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d5ff2fd4f9bd3360974d93c457e541cb2f96dc5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575379"
---
# <span data-ttu-id="463a9-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="463a9-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="463a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="463a9-102">SYNOPSIS</span></span>
<span data-ttu-id="463a9-103">Skapar ett nytt Server dels proxyobjekt.</span><span class="sxs-lookup"><span data-stu-id="463a9-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="463a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="463a9-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="463a9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="463a9-105">DESCRIPTION</span></span>
<span data-ttu-id="463a9-106">Skapar ett nytt backend-proxyobjekt som kan vara piped när du skapar en ny backend-enhet.</span><span class="sxs-lookup"><span data-stu-id="463a9-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="463a9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="463a9-107">EXAMPLES</span></span>

### <span data-ttu-id="463a9-108">Skapa ett In-Memory objekt i en del av Server delen</span><span class="sxs-lookup"><span data-stu-id="463a9-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzureRmApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="463a9-109">Skapar ett dataservers-proxyobjekt och konfigurerar Server delen</span><span class="sxs-lookup"><span data-stu-id="463a9-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="463a9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="463a9-110">PARAMETERS</span></span>

### <span data-ttu-id="463a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463a9-111">-DefaultProfile</span></span>
<span data-ttu-id="463a9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="463a9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="463a9-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="463a9-113">-ProxyCredential</span></span>
<span data-ttu-id="463a9-114">Autentiseringsuppgifter som används för att ansluta till backend-proxyservern.</span><span class="sxs-lookup"><span data-stu-id="463a9-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="463a9-115">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="463a9-115">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="463a9-116">-URL</span><span class="sxs-lookup"><span data-stu-id="463a9-116">-Url</span></span>
<span data-ttu-id="463a9-117">URL-adressen till den proxyserver som ska användas vid vidarekoppling av samtal till Server delen.</span><span class="sxs-lookup"><span data-stu-id="463a9-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="463a9-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="463a9-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="463a9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463a9-119">CommonParameters</span></span>
<span data-ttu-id="463a9-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="463a9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463a9-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="463a9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463a9-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="463a9-122">INPUTS</span></span>

### <span data-ttu-id="463a9-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="463a9-123">None</span></span>

## <span data-ttu-id="463a9-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="463a9-124">OUTPUTS</span></span>

### <span data-ttu-id="463a9-125">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="463a9-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="463a9-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="463a9-126">NOTES</span></span>

## <span data-ttu-id="463a9-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="463a9-127">RELATED LINKS</span></span>

[<span data-ttu-id="463a9-128">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="463a9-128">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="463a9-129">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="463a9-129">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="463a9-130">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="463a9-130">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="463a9-131">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="463a9-131">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="463a9-132">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="463a9-132">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
