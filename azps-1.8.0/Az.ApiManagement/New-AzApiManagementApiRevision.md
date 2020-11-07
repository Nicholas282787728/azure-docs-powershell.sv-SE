---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 81a80acdfb89f30cc1add6b1cfc10bcd7d745dfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743372"
---
# <span data-ttu-id="167e4-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="167e4-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="167e4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="167e4-102">SYNOPSIS</span></span>
<span data-ttu-id="167e4-103">Skapar en ny version av ett befintligt API.</span><span class="sxs-lookup"><span data-stu-id="167e4-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="167e4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="167e4-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="167e4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="167e4-105">DESCRIPTION</span></span>

<span data-ttu-id="167e4-106">Cmdleten **New-AzApiManagementApiRevision** skapar en API-revision för en befintlig API i API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="167e4-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="167e4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="167e4-107">EXAMPLES</span></span>

### <span data-ttu-id="167e4-108">Exempel 1: skapa en API-revision för ett API</span><span class="sxs-lookup"><span data-stu-id="167e4-108">Example 1: Create an API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $ApiMgmtContext  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6


ApiId                         : 5adf6fbf0faadf3ad8558065;rev=6
Name                          : httpbin.org
Description                   : API Management facade for a very handy and free online HTTP tool.
ServiceUrl                    : https://httpbin.org/
Path                          : httpbin
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         : contoso-oauth
AuthorizationScope            : contoso-oauth
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 6
ApiVersion                    : v1
IsCurrent                     : False
IsOnline                      : False
Id                            : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065;rev=6
ResourceGroupName             : Api-Default-WestUS
ServiceName                   : contoso
```

<span data-ttu-id="167e4-109">Det här kommandot skapar en API-revision `2` av `echo-api` API: t.</span><span class="sxs-lookup"><span data-stu-id="167e4-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

## <span data-ttu-id="167e4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="167e4-110">PARAMETERS</span></span>

### <span data-ttu-id="167e4-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="167e4-111">-ApiId</span></span>
<span data-ttu-id="167e4-112">ID för API vars ändring ska skapas.</span><span class="sxs-lookup"><span data-stu-id="167e4-112">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="167e4-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="167e4-113">-ApiRevision</span></span>
<span data-ttu-id="167e4-114">Revisions-ID för API: t.</span><span class="sxs-lookup"><span data-stu-id="167e4-114">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="167e4-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="167e4-115">-Context</span></span>
<span data-ttu-id="167e4-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="167e4-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="167e4-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="167e4-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="167e4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="167e4-118">-DefaultProfile</span></span>
<span data-ttu-id="167e4-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="167e4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="167e4-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="167e4-120">-Confirm</span></span>
<span data-ttu-id="167e4-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="167e4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="167e4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="167e4-122">-WhatIf</span></span>
<span data-ttu-id="167e4-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="167e4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="167e4-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="167e4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="167e4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="167e4-125">CommonParameters</span></span>
<span data-ttu-id="167e4-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="167e4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="167e4-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="167e4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="167e4-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="167e4-128">INPUTS</span></span>

### <span data-ttu-id="167e4-129">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="167e4-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="167e4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="167e4-130">System.String</span></span>

## <span data-ttu-id="167e4-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="167e4-131">OUTPUTS</span></span>

### <span data-ttu-id="167e4-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="167e4-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="167e4-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="167e4-133">NOTES</span></span>

## <span data-ttu-id="167e4-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="167e4-134">RELATED LINKS</span></span>

[<span data-ttu-id="167e4-135">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="167e4-135">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="167e4-136">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="167e4-136">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="167e4-137">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="167e4-137">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
