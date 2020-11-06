---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 3c37376aa475e8b0797d4ff4433ab54a11d2b6bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579871"
---
# <span data-ttu-id="4d50c-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4d50c-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="4d50c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d50c-102">SYNOPSIS</span></span>
<span data-ttu-id="4d50c-103">Hämtar en Authorization Server för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="4d50c-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d50c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d50c-104">SYNTAX</span></span>

### <span data-ttu-id="4d50c-105">Hämta all auktoriseringsprincip (standard)</span><span class="sxs-lookup"><span data-stu-id="4d50c-105">Get all authorization server (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d50c-106">Skaffa efter ID</span><span class="sxs-lookup"><span data-stu-id="4d50c-106">Get by Id</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d50c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d50c-107">DESCRIPTION</span></span>
<span data-ttu-id="4d50c-108">Cmdleten **Get-AzureRmApiManagementAuthorizationServer** får alla auktoriseringsregler för Azure API Management eller angivna fjärrinstallationsservrar.</span><span class="sxs-lookup"><span data-stu-id="4d50c-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="4d50c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d50c-109">EXAMPLES</span></span>

### <span data-ttu-id="4d50c-110">Exempel 1: Hämta alla auktoriseringsregler</span><span class="sxs-lookup"><span data-stu-id="4d50c-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="4d50c-111">Det här kommandot får alla fjärrinstallationsservrar för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="4d50c-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="4d50c-112">Exempel 2: skaffa en angiven auktoriseringsregel</span><span class="sxs-lookup"><span data-stu-id="4d50c-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="4d50c-113">Det här kommandot hämtar den angivna auktoriseringsservern.</span><span class="sxs-lookup"><span data-stu-id="4d50c-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="4d50c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d50c-114">PARAMETERS</span></span>

### <span data-ttu-id="4d50c-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4d50c-115">-Context</span></span>
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

### <span data-ttu-id="4d50c-116">-ServerId</span><span class="sxs-lookup"><span data-stu-id="4d50c-116">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d50c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d50c-117">-DefaultProfile</span></span>
<span data-ttu-id="4d50c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d50c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d50c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d50c-119">CommonParameters</span></span>
<span data-ttu-id="4d50c-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d50c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d50c-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d50c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d50c-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d50c-122">INPUTS</span></span>

## <span data-ttu-id="4d50c-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d50c-123">OUTPUTS</span></span>

### <span data-ttu-id="4d50c-124">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthrozationServer></span><span class="sxs-lookup"><span data-stu-id="4d50c-124">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer></span></span>

## <span data-ttu-id="4d50c-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d50c-125">NOTES</span></span>

## <span data-ttu-id="4d50c-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d50c-126">RELATED LINKS</span></span>

[<span data-ttu-id="4d50c-127">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4d50c-127">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="4d50c-128">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4d50c-128">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="4d50c-129">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4d50c-129">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


