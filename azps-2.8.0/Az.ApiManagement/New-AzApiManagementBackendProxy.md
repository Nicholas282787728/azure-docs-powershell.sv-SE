---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: 2ce3863a546af0f8c9da3c37a75b540d2a859da1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745786"
---
# <span data-ttu-id="8fe4b-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8fe4b-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="8fe4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8fe4b-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe4b-103">Skapar ett nytt Server dels proxyobjekt.</span><span class="sxs-lookup"><span data-stu-id="8fe4b-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="8fe4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8fe4b-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fe4b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8fe4b-105">DESCRIPTION</span></span>
<span data-ttu-id="8fe4b-106">Skapar ett nytt backend-proxyobjekt som kan vara piped när du skapar en ny backend-enhet.</span><span class="sxs-lookup"><span data-stu-id="8fe4b-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="8fe4b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8fe4b-107">EXAMPLES</span></span>

### <span data-ttu-id="8fe4b-108">Skapa ett In-Memory objekt i en del av Server delen</span><span class="sxs-lookup"><span data-stu-id="8fe4b-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="8fe4b-109">Skapar ett dataservers-proxyobjekt och konfigurerar Server delen</span><span class="sxs-lookup"><span data-stu-id="8fe4b-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="8fe4b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8fe4b-110">PARAMETERS</span></span>

### <span data-ttu-id="8fe4b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe4b-111">-DefaultProfile</span></span>
<span data-ttu-id="8fe4b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8fe4b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fe4b-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="8fe4b-113">-ProxyCredential</span></span>
<span data-ttu-id="8fe4b-114">Autentiseringsuppgifter som används för att ansluta till backend-proxyservern.</span><span class="sxs-lookup"><span data-stu-id="8fe4b-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="8fe4b-115">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="8fe4b-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="8fe4b-116">-URL</span><span class="sxs-lookup"><span data-stu-id="8fe4b-116">-Url</span></span>
<span data-ttu-id="8fe4b-117">URL-adressen till den proxyserver som ska användas vid vidarekoppling av samtal till Server delen.</span><span class="sxs-lookup"><span data-stu-id="8fe4b-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="8fe4b-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="8fe4b-118">This parameter is required.</span></span>

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

### <span data-ttu-id="8fe4b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe4b-119">CommonParameters</span></span>
<span data-ttu-id="8fe4b-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fe4b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe4b-121">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fe4b-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe4b-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8fe4b-122">INPUTS</span></span>

### <span data-ttu-id="8fe4b-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="8fe4b-123">None</span></span>

## <span data-ttu-id="8fe4b-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8fe4b-124">OUTPUTS</span></span>

### <span data-ttu-id="8fe4b-125">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8fe4b-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="8fe4b-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8fe4b-126">NOTES</span></span>

## <span data-ttu-id="8fe4b-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8fe4b-127">RELATED LINKS</span></span>

[<span data-ttu-id="8fe4b-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8fe4b-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="8fe4b-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8fe4b-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="8fe4b-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="8fe4b-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="8fe4b-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8fe4b-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="8fe4b-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8fe4b-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
