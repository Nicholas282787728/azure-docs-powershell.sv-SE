---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: f816488e6334c0e9c410bb1c24f46501a1fefe85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743373"
---
# <span data-ttu-id="aafa3-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aafa3-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="aafa3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aafa3-102">SYNOPSIS</span></span>
<span data-ttu-id="aafa3-103">Skapar en API-version av en API-revision</span><span class="sxs-lookup"><span data-stu-id="aafa3-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="aafa3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aafa3-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aafa3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aafa3-105">DESCRIPTION</span></span>

<span data-ttu-id="aafa3-106">Cmdleten **New-AzApiManagementApiRelease** skapar en API-version för en API-revision i API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="aafa3-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="aafa3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aafa3-107">EXAMPLES</span></span>

### <span data-ttu-id="aafa3-108">Exempel 1: skapa en API-utgåva för en API-revision</span><span class="sxs-lookup"><span data-stu-id="aafa3-108">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


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

<span data-ttu-id="aafa3-109">Det här kommandot skapar en API-version av en revidering `2` av `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="aafa3-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="aafa3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aafa3-110">PARAMETERS</span></span>

### <span data-ttu-id="aafa3-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="aafa3-111">-ApiId</span></span>
<span data-ttu-id="aafa3-112">Identifierare för nytt API.</span><span class="sxs-lookup"><span data-stu-id="aafa3-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="aafa3-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="aafa3-113">-ApiRevision</span></span>
<span data-ttu-id="aafa3-114">ID för API-revision.</span><span class="sxs-lookup"><span data-stu-id="aafa3-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="aafa3-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="aafa3-115">-Context</span></span>
<span data-ttu-id="aafa3-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="aafa3-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="aafa3-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="aafa3-117">This parameter is required.</span></span>

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

### <span data-ttu-id="aafa3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aafa3-118">-DefaultProfile</span></span>
<span data-ttu-id="aafa3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aafa3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aafa3-120">-Obs!</span><span class="sxs-lookup"><span data-stu-id="aafa3-120">-Note</span></span>
<span data-ttu-id="aafa3-121">API-versions anteckningar.</span><span class="sxs-lookup"><span data-stu-id="aafa3-121">Api Release Notes.</span></span> <span data-ttu-id="aafa3-122">Den här parametern är valfri</span><span class="sxs-lookup"><span data-stu-id="aafa3-122">This parameter is optional</span></span>

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

### <span data-ttu-id="aafa3-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="aafa3-123">-ReleaseId</span></span>
<span data-ttu-id="aafa3-124">Identifierare för API-versionen.</span><span class="sxs-lookup"><span data-stu-id="aafa3-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="aafa3-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="aafa3-125">This parameter is optional.</span></span>
<span data-ttu-id="aafa3-126">Om du inte anger ett angivet ID.</span><span class="sxs-lookup"><span data-stu-id="aafa3-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="aafa3-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aafa3-127">-Confirm</span></span>
<span data-ttu-id="aafa3-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aafa3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aafa3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aafa3-129">-WhatIf</span></span>
<span data-ttu-id="aafa3-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aafa3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aafa3-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aafa3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aafa3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aafa3-132">CommonParameters</span></span>
<span data-ttu-id="aafa3-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aafa3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aafa3-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aafa3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aafa3-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aafa3-135">INPUTS</span></span>

### <span data-ttu-id="aafa3-136">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aafa3-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aafa3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="aafa3-137">System.String</span></span>

## <span data-ttu-id="aafa3-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aafa3-138">OUTPUTS</span></span>

### <span data-ttu-id="aafa3-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aafa3-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="aafa3-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aafa3-140">NOTES</span></span>

## <span data-ttu-id="aafa3-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aafa3-141">RELATED LINKS</span></span>

[<span data-ttu-id="aafa3-142">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aafa3-142">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="aafa3-143">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aafa3-143">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="aafa3-144">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aafa3-144">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)