---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 784480b56a868f84f8f79a35bf7ab2c1ba2e9fbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745799"
---
# <span data-ttu-id="b76e6-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b76e6-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="b76e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b76e6-102">SYNOPSIS</span></span>
<span data-ttu-id="b76e6-103">Skapar en API-version av en API-revision</span><span class="sxs-lookup"><span data-stu-id="b76e6-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="b76e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b76e6-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b76e6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b76e6-105">DESCRIPTION</span></span>

<span data-ttu-id="b76e6-106">Cmdleten **New-AzApiManagementApiRelease** skapar en API-version för en API-revision i API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="b76e6-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="b76e6-107">En version används för att göra API-revisionen som aktuell ändring.</span><span class="sxs-lookup"><span data-stu-id="b76e6-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="b76e6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b76e6-108">EXAMPLES</span></span>

### <span data-ttu-id="b76e6-109">Exempel 1: skapa en API-utgåva för en API-revision</span><span class="sxs-lookup"><span data-stu-id="b76e6-109">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="b76e6-110">Det här kommandot skapar en API-version av en revidering `2` av `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="b76e6-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="b76e6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b76e6-111">PARAMETERS</span></span>

### <span data-ttu-id="b76e6-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b76e6-112">-ApiId</span></span>
<span data-ttu-id="b76e6-113">Identifierare för nytt API.</span><span class="sxs-lookup"><span data-stu-id="b76e6-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="b76e6-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="b76e6-114">-ApiRevision</span></span>
<span data-ttu-id="b76e6-115">ID för API-revision.</span><span class="sxs-lookup"><span data-stu-id="b76e6-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="b76e6-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b76e6-116">-Context</span></span>
<span data-ttu-id="b76e6-117">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b76e6-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b76e6-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b76e6-118">This parameter is required.</span></span>

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

### <span data-ttu-id="b76e6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76e6-119">-DefaultProfile</span></span>
<span data-ttu-id="b76e6-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b76e6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b76e6-121">-Obs!</span><span class="sxs-lookup"><span data-stu-id="b76e6-121">-Note</span></span>
<span data-ttu-id="b76e6-122">API-versions anteckningar.</span><span class="sxs-lookup"><span data-stu-id="b76e6-122">Api Release Notes.</span></span> <span data-ttu-id="b76e6-123">Den här parametern är valfri</span><span class="sxs-lookup"><span data-stu-id="b76e6-123">This parameter is optional</span></span>

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

### <span data-ttu-id="b76e6-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="b76e6-124">-ReleaseId</span></span>
<span data-ttu-id="b76e6-125">Identifierare för API-versionen.</span><span class="sxs-lookup"><span data-stu-id="b76e6-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="b76e6-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b76e6-126">This parameter is optional.</span></span>
<span data-ttu-id="b76e6-127">Om du inte anger ett angivet ID.</span><span class="sxs-lookup"><span data-stu-id="b76e6-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="b76e6-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b76e6-128">-Confirm</span></span>
<span data-ttu-id="b76e6-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b76e6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b76e6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b76e6-130">-WhatIf</span></span>
<span data-ttu-id="b76e6-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b76e6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b76e6-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b76e6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b76e6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76e6-133">CommonParameters</span></span>
<span data-ttu-id="b76e6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b76e6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76e6-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b76e6-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76e6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b76e6-136">INPUTS</span></span>

### <span data-ttu-id="b76e6-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b76e6-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b76e6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b76e6-138">System.String</span></span>

## <span data-ttu-id="b76e6-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b76e6-139">OUTPUTS</span></span>

### <span data-ttu-id="b76e6-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b76e6-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="b76e6-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b76e6-141">NOTES</span></span>

## <span data-ttu-id="b76e6-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b76e6-142">RELATED LINKS</span></span>

[<span data-ttu-id="b76e6-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b76e6-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="b76e6-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b76e6-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="b76e6-145">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b76e6-145">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)