---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 4453b7fc3e13f4de2632c41cea966fdada1d84f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585216"
---
# <span data-ttu-id="59cff-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="59cff-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="59cff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59cff-102">SYNOPSIS</span></span>
<span data-ttu-id="59cff-103">Skapar ett nytt kontrakt för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="59cff-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59cff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59cff-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59cff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59cff-105">DESCRIPTION</span></span>
<span data-ttu-id="59cff-106">Skapar ett nytt kontrakt för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="59cff-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="59cff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59cff-107">EXAMPLES</span></span>

### <span data-ttu-id="59cff-108">Skapa en server dels referenser In-Memory objekt</span><span class="sxs-lookup"><span data-stu-id="59cff-108">Create a Backend Credentials In-Memory Object</span></span>
```
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="59cff-109">Skapar ett kontrakt för inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="59cff-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="59cff-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59cff-110">PARAMETERS</span></span>

### <span data-ttu-id="59cff-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="59cff-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="59cff-112">Huvud tillstånd som används för Server delen.</span><span class="sxs-lookup"><span data-stu-id="59cff-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="59cff-113">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="59cff-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="59cff-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="59cff-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="59cff-115">Godkännande schema som används för Server delen.</span><span class="sxs-lookup"><span data-stu-id="59cff-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="59cff-116">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="59cff-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="59cff-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="59cff-117">-CertificateThumbprint</span></span>
<span data-ttu-id="59cff-118">Thumbprints för klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="59cff-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="59cff-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="59cff-119">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59cff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59cff-120">-DefaultProfile</span></span>
<span data-ttu-id="59cff-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59cff-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59cff-122">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="59cff-122">-Header</span></span>
<span data-ttu-id="59cff-123">Rubrik parameter värden som accepteras av Server delen.</span><span class="sxs-lookup"><span data-stu-id="59cff-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="59cff-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="59cff-124">This parameter is optional.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59cff-125">-Fråga</span><span class="sxs-lookup"><span data-stu-id="59cff-125">-Query</span></span>
<span data-ttu-id="59cff-126">Parameter värden för frågor som accepteras av Server delen.</span><span class="sxs-lookup"><span data-stu-id="59cff-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="59cff-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="59cff-127">This parameter is optional.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59cff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59cff-128">CommonParameters</span></span>
<span data-ttu-id="59cff-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59cff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59cff-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59cff-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59cff-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59cff-131">INPUTS</span></span>

### <span data-ttu-id="59cff-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="59cff-132">None</span></span>
<span data-ttu-id="59cff-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="59cff-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59cff-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59cff-134">OUTPUTS</span></span>

### <span data-ttu-id="59cff-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="59cff-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="59cff-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59cff-136">NOTES</span></span>

## <span data-ttu-id="59cff-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59cff-137">RELATED LINKS</span></span>

[<span data-ttu-id="59cff-138">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="59cff-138">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="59cff-139">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="59cff-139">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="59cff-140">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="59cff-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="59cff-141">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="59cff-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="59cff-142">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="59cff-142">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
