---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: cb7fbfe4ba4fdf09b9012ddc5be8028af0bd80c1
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93586624"
---
# <span data-ttu-id="24936-101">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="24936-101">New-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="24936-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24936-102">SYNOPSIS</span></span>
<span data-ttu-id="24936-103">Skapar en API-version av en API-revision</span><span class="sxs-lookup"><span data-stu-id="24936-103">Creates an API Release of an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24936-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24936-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24936-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24936-105">DESCRIPTION</span></span>

<span data-ttu-id="24936-106">Cmdleten **New-AzureRmApiManagementApiRelease** skapar en API-version för en API-revision i API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="24936-106">The **New-AzureRmApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="24936-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24936-107">EXAMPLES</span></span>

### <span data-ttu-id="24936-108">Exempel 1: skapa en API-utgåva för en API-revision</span><span class="sxs-lookup"><span data-stu-id="24936-108">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


ReleaseId         : 7e4d3fbb43c146c4bf406499ef9411f4
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 1:16:29 AM
UpdatedDateTime   : 5/17/2018 1:16:29 AM
Notes             : Releasing version 6
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/7e4d3fbb43c146c4bf40649
                    9ef9411f4
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="24936-109">Det här kommandot skapar en API-version av en revidering `2` av `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="24936-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="24936-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24936-110">PARAMETERS</span></span>

### <span data-ttu-id="24936-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="24936-111">-ApiId</span></span>
<span data-ttu-id="24936-112">Identifierare för nytt API.</span><span class="sxs-lookup"><span data-stu-id="24936-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="24936-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="24936-113">-ApiRevision</span></span>
<span data-ttu-id="24936-114">ID för API-revision.</span><span class="sxs-lookup"><span data-stu-id="24936-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="24936-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="24936-115">-Context</span></span>
<span data-ttu-id="24936-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="24936-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="24936-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="24936-117">This parameter is required.</span></span>

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

### <span data-ttu-id="24936-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24936-118">-DefaultProfile</span></span>
<span data-ttu-id="24936-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24936-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24936-120">-Obs!</span><span class="sxs-lookup"><span data-stu-id="24936-120">-Note</span></span>
<span data-ttu-id="24936-121">API-versions anteckningar.</span><span class="sxs-lookup"><span data-stu-id="24936-121">Api Release Notes.</span></span> <span data-ttu-id="24936-122">Den här parametern är valfri</span><span class="sxs-lookup"><span data-stu-id="24936-122">This parameter is optional</span></span>

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

### <span data-ttu-id="24936-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="24936-123">-ReleaseId</span></span>
<span data-ttu-id="24936-124">Identifierare för API-versionen.</span><span class="sxs-lookup"><span data-stu-id="24936-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="24936-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="24936-125">This parameter is optional.</span></span>
<span data-ttu-id="24936-126">Om du inte anger ett angivet ID.</span><span class="sxs-lookup"><span data-stu-id="24936-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="24936-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24936-127">-Confirm</span></span>
<span data-ttu-id="24936-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24936-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24936-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24936-129">-WhatIf</span></span>
<span data-ttu-id="24936-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24936-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24936-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24936-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24936-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24936-132">CommonParameters</span></span>
<span data-ttu-id="24936-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24936-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24936-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24936-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24936-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24936-135">INPUTS</span></span>

### <span data-ttu-id="24936-136">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="24936-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="24936-137">Parametrar: kontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24936-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="24936-138">System. String</span><span class="sxs-lookup"><span data-stu-id="24936-138">System.String</span></span>

## <span data-ttu-id="24936-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24936-139">OUTPUTS</span></span>

### <span data-ttu-id="24936-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="24936-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="24936-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24936-141">NOTES</span></span>

## <span data-ttu-id="24936-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24936-142">RELATED LINKS</span></span>

[<span data-ttu-id="24936-143">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="24936-143">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="24936-144">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="24936-144">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="24936-145">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="24936-145">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
