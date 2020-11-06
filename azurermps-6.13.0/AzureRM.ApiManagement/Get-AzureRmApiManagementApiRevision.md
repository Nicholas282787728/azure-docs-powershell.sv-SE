---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: f57a95e97c0ec74e7e45338e15a028feab60849b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579136"
---
# <span data-ttu-id="59db7-101">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="59db7-101">Get-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="59db7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59db7-102">SYNOPSIS</span></span>
<span data-ttu-id="59db7-103">Hämtar information om alla API-ändringar i ett API</span><span class="sxs-lookup"><span data-stu-id="59db7-103">Gets details of all the API Revisions of an API</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59db7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59db7-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59db7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59db7-105">DESCRIPTION</span></span>
<span data-ttu-id="59db7-106">Cmdleten **Get-AzureRmApiManagementApiRevision** får information om alla revisioner av ett API</span><span class="sxs-lookup"><span data-stu-id="59db7-106">The **Get-AzureRmApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="59db7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59db7-107">EXAMPLES</span></span>

### <span data-ttu-id="59db7-108">Exempel 1: få alla API-revisioner av ett API</span><span class="sxs-lookup"><span data-stu-id="59db7-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=3
ApiRevision     : 3
CreatedDateTime : 4/26/2018 10:57:42 PM
UpdatedDateTime : 4/26/2018 10:57:42 PM
Description     : ddsds
PrivateUrl      : /httpbin/v1;rev=3
IsOnline        : True
IsCurrent       : False

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=2
ApiRevision     : 2
CreatedDateTime : 4/26/2018 10:57:33 PM
UpdatedDateTime : 4/26/2018 10:57:33 PM
Description     : AA
PrivateUrl      : /httpbin/v1
IsOnline        : True
IsCurrent       : True

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=1
ApiRevision     : 1
CreatedDateTime : 4/24/2018 5:56:17 PM
UpdatedDateTime : 5/9/2018 9:29:06 PM
Description     :
PrivateUrl      : /httpbin/v1;rev=1
IsOnline        : True
IsCurrent       : False
```

<span data-ttu-id="59db7-109">Det här kommandot får hela API-revisionen av angivet API för viss ApiManagement kontext.</span><span class="sxs-lookup"><span data-stu-id="59db7-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="59db7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59db7-110">PARAMETERS</span></span>

### <span data-ttu-id="59db7-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="59db7-111">-ApiId</span></span>
<span data-ttu-id="59db7-112">API-identifierare vars ändringar vi vill visa.</span><span class="sxs-lookup"><span data-stu-id="59db7-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="59db7-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="59db7-113">This parameter is required.</span></span>

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

### <span data-ttu-id="59db7-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="59db7-114">-ApiRevision</span></span>
<span data-ttu-id="59db7-115">Revisions-ID för den speciella API-revision.</span><span class="sxs-lookup"><span data-stu-id="59db7-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="59db7-116">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="59db7-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="59db7-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="59db7-117">-Context</span></span>
<span data-ttu-id="59db7-118">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="59db7-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="59db7-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="59db7-119">This parameter is required.</span></span>

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

### <span data-ttu-id="59db7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59db7-120">-DefaultProfile</span></span>
<span data-ttu-id="59db7-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59db7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59db7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59db7-122">CommonParameters</span></span>
<span data-ttu-id="59db7-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59db7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59db7-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59db7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59db7-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59db7-125">INPUTS</span></span>

### <span data-ttu-id="59db7-126">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="59db7-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="59db7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="59db7-127">System.String</span></span>

## <span data-ttu-id="59db7-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59db7-128">OUTPUTS</span></span>

### <span data-ttu-id="59db7-129">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="59db7-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="59db7-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59db7-130">NOTES</span></span>

## <span data-ttu-id="59db7-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59db7-131">RELATED LINKS</span></span>
