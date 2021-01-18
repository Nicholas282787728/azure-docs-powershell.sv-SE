---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525116"
---
# <span data-ttu-id="375f8-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="375f8-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="375f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="375f8-102">SYNOPSIS</span></span>
<span data-ttu-id="375f8-103">Få information om Server delen.</span><span class="sxs-lookup"><span data-stu-id="375f8-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="375f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="375f8-104">SYNTAX</span></span>

### <span data-ttu-id="375f8-105">ContextParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="375f8-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="375f8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="375f8-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="375f8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="375f8-107">DESCRIPTION</span></span>
<span data-ttu-id="375f8-108">Få information om Server delen.</span><span class="sxs-lookup"><span data-stu-id="375f8-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="375f8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="375f8-109">EXAMPLES</span></span>

### <span data-ttu-id="375f8-110">Exempel 1: få alla bakände</span><span class="sxs-lookup"><span data-stu-id="375f8-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="375f8-111">Hämtar en lista över alla bakände som har kon figurer ATS i API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="375f8-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="375f8-112">Exempel 2: Hämta Server delen som anges av ID 123</span><span class="sxs-lookup"><span data-stu-id="375f8-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="375f8-113">Få information om den angivna Server delen som identifieras av identifieraren ' 123 '</span><span class="sxs-lookup"><span data-stu-id="375f8-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="375f8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="375f8-114">PARAMETERS</span></span>

### <span data-ttu-id="375f8-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="375f8-115">-BackendId</span></span>
<span data-ttu-id="375f8-116">Identifierare för en server del.</span><span class="sxs-lookup"><span data-stu-id="375f8-116">Identifier of a backend.</span></span>
<span data-ttu-id="375f8-117">Om det här alternativet väljs kommer att försöka hitta server delen av identifieraren.</span><span class="sxs-lookup"><span data-stu-id="375f8-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="375f8-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="375f8-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="375f8-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="375f8-119">-Context</span></span>
<span data-ttu-id="375f8-120">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="375f8-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="375f8-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="375f8-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="375f8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="375f8-122">-DefaultProfile</span></span>
<span data-ttu-id="375f8-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="375f8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="375f8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="375f8-124">-ResourceId</span></span>
<span data-ttu-id="375f8-125">Server delen för arm-resursen.</span><span class="sxs-lookup"><span data-stu-id="375f8-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="375f8-126">Om det här alternativet väljs kommer att försöka hitta server delen av identifieraren.</span><span class="sxs-lookup"><span data-stu-id="375f8-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="375f8-127">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="375f8-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="375f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="375f8-128">CommonParameters</span></span>
<span data-ttu-id="375f8-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="375f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="375f8-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="375f8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="375f8-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="375f8-131">INPUTS</span></span>

### <span data-ttu-id="375f8-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="375f8-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="375f8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="375f8-133">System.String</span></span>

## <span data-ttu-id="375f8-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="375f8-134">OUTPUTS</span></span>

### <span data-ttu-id="375f8-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="375f8-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="375f8-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="375f8-136">NOTES</span></span>

## <span data-ttu-id="375f8-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="375f8-137">RELATED LINKS</span></span>

[<span data-ttu-id="375f8-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="375f8-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="375f8-139">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="375f8-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="375f8-140">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="375f8-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="375f8-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="375f8-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="375f8-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="375f8-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
