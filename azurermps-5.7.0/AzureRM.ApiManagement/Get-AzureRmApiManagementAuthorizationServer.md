---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 651ef4c0c44b7e3269eb300dcfa098c39415f77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756518"
---
# <span data-ttu-id="7e3b8-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7e3b8-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="7e3b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3b8-103">Hämtar en Authorization Server för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="7e3b8-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e3b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e3b8-104">SYNTAX</span></span>

### <span data-ttu-id="7e3b8-105">GetAllAuthorizationServers (standard)</span><span class="sxs-lookup"><span data-stu-id="7e3b8-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e3b8-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="7e3b8-106">GetByServerId</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e3b8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e3b8-107">DESCRIPTION</span></span>
<span data-ttu-id="7e3b8-108">Cmdleten **Get-AzureRmApiManagementAuthorizationServer** får alla auktoriseringsregler för Azure API Management eller angivna fjärrinstallationsservrar.</span><span class="sxs-lookup"><span data-stu-id="7e3b8-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="7e3b8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e3b8-109">EXAMPLES</span></span>

### <span data-ttu-id="7e3b8-110">Exempel 1: Hämta alla auktoriseringsregler</span><span class="sxs-lookup"><span data-stu-id="7e3b8-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="7e3b8-111">Det här kommandot får alla fjärrinstallationsservrar för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="7e3b8-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="7e3b8-112">Exempel 2: skaffa en angiven auktoriseringsregel</span><span class="sxs-lookup"><span data-stu-id="7e3b8-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="7e3b8-113">Det här kommandot hämtar den angivna auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="7e3b8-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="7e3b8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e3b8-114">PARAMETERS</span></span>

### <span data-ttu-id="7e3b8-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7e3b8-115">-Context</span></span>
```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e3b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3b8-116">-DefaultProfile</span></span>
<span data-ttu-id="7e3b8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e3b8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="7e3b8-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="7e3b8-118">-ServerId</span></span>
```yaml
Type: String
Parameter Sets: GetByServerId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e3b8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3b8-119">CommonParameters</span></span>
<span data-ttu-id="7e3b8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e3b8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3b8-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e3b8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3b8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e3b8-122">INPUTS</span></span>

### <span data-ttu-id="7e3b8-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="7e3b8-123">None</span></span>
<span data-ttu-id="7e3b8-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7e3b8-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e3b8-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e3b8-125">OUTPUTS</span></span>

### <span data-ttu-id="7e3b8-126">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer</span><span class="sxs-lookup"><span data-stu-id="7e3b8-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>
<span data-ttu-id="7e3b8-127">Information om Auktoriseringsservern i en given API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="7e3b8-127">The details of the Authorization Server in a given Api Management service.</span></span>

### <span data-ttu-id="7e3b8-128">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer></span><span class="sxs-lookup"><span data-stu-id="7e3b8-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer></span></span>
<span data-ttu-id="7e3b8-129">Listan med auktoriseringsregler i en given API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="7e3b8-129">The list of Authorization Server in a given Api Management service.</span></span>

## <span data-ttu-id="7e3b8-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e3b8-130">NOTES</span></span>

## <span data-ttu-id="7e3b8-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e3b8-131">RELATED LINKS</span></span>

[<span data-ttu-id="7e3b8-132">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7e3b8-132">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="7e3b8-133">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7e3b8-133">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="7e3b8-134">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7e3b8-134">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


