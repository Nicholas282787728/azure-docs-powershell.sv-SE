---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: 5abd20ac1515cb2d7de96d7f5ed42938cee09a57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745852"
---
# <span data-ttu-id="eaee4-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="eaee4-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="eaee4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eaee4-102">SYNOPSIS</span></span>
<span data-ttu-id="eaee4-103">Hämtar information om alla API-ändringar i ett API</span><span class="sxs-lookup"><span data-stu-id="eaee4-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="eaee4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eaee4-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaee4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eaee4-105">DESCRIPTION</span></span>
<span data-ttu-id="eaee4-106">Cmdleten **Get-AzApiManagementApiRevision** får information om alla revisioner av ett API</span><span class="sxs-lookup"><span data-stu-id="eaee4-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="eaee4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eaee4-107">EXAMPLES</span></span>

### <span data-ttu-id="eaee4-108">Exempel 1: få alla API-revisioner av ett API</span><span class="sxs-lookup"><span data-stu-id="eaee4-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

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

<span data-ttu-id="eaee4-109">Det här kommandot får hela API-revisionen av angivet API för viss ApiManagement kontext.</span><span class="sxs-lookup"><span data-stu-id="eaee4-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="eaee4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eaee4-110">PARAMETERS</span></span>

### <span data-ttu-id="eaee4-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="eaee4-111">-ApiId</span></span>
<span data-ttu-id="eaee4-112">API-identifierare vars ändringar vi vill visa.</span><span class="sxs-lookup"><span data-stu-id="eaee4-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="eaee4-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="eaee4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="eaee4-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="eaee4-114">-ApiRevision</span></span>
<span data-ttu-id="eaee4-115">Revisions-ID för den speciella API-revision.</span><span class="sxs-lookup"><span data-stu-id="eaee4-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="eaee4-116">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="eaee4-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="eaee4-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="eaee4-117">-Context</span></span>
<span data-ttu-id="eaee4-118">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="eaee4-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="eaee4-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="eaee4-119">This parameter is required.</span></span>

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

### <span data-ttu-id="eaee4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaee4-120">-DefaultProfile</span></span>
<span data-ttu-id="eaee4-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eaee4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaee4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaee4-122">CommonParameters</span></span>
<span data-ttu-id="eaee4-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaee4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaee4-124">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eaee4-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaee4-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eaee4-125">INPUTS</span></span>

### <span data-ttu-id="eaee4-126">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="eaee4-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="eaee4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="eaee4-127">System.String</span></span>

## <span data-ttu-id="eaee4-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eaee4-128">OUTPUTS</span></span>

### <span data-ttu-id="eaee4-129">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="eaee4-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="eaee4-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eaee4-130">NOTES</span></span>

## <span data-ttu-id="eaee4-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eaee4-131">RELATED LINKS</span></span>
