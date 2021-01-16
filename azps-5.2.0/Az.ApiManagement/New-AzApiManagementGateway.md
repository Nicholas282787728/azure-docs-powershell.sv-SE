---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392683"
---
# <span data-ttu-id="d860f-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="d860f-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="d860f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d860f-102">SYNOPSIS</span></span>
<span data-ttu-id="d860f-103">Skapar ny gateway-enhet.</span><span class="sxs-lookup"><span data-stu-id="d860f-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="d860f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d860f-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d860f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d860f-105">DESCRIPTION</span></span>
<span data-ttu-id="d860f-106">Cmdleten **New-AzApiManagementGateway** skapar en ny gateway-enhet.</span><span class="sxs-lookup"><span data-stu-id="d860f-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="d860f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d860f-107">EXAMPLES</span></span>

### <span data-ttu-id="d860f-108">Exempel 1: skapa en gateway</span><span class="sxs-lookup"><span data-stu-id="d860f-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="d860f-109">Det här kommandot skapar en gateway.</span><span class="sxs-lookup"><span data-stu-id="d860f-109">This command creates a gateway.</span></span>

## <span data-ttu-id="d860f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d860f-110">PARAMETERS</span></span>

### <span data-ttu-id="d860f-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d860f-111">-Context</span></span>
<span data-ttu-id="d860f-112">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d860f-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d860f-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d860f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d860f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d860f-114">-DefaultProfile</span></span>
<span data-ttu-id="d860f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d860f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d860f-116">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d860f-116">-Description</span></span>
<span data-ttu-id="d860f-117">Beskrivning av gatewayen.</span><span class="sxs-lookup"><span data-stu-id="d860f-117">Gateway description.</span></span>
<span data-ttu-id="d860f-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d860f-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="d860f-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="d860f-119">-GatewayId</span></span>
<span data-ttu-id="d860f-120">Identifierare för ny Gateway.</span><span class="sxs-lookup"><span data-stu-id="d860f-120">Identifier of new gateway.</span></span>
<span data-ttu-id="d860f-121">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d860f-121">This parameter is optional.</span></span>
<span data-ttu-id="d860f-122">Om det inte anges kommer att genereras.</span><span class="sxs-lookup"><span data-stu-id="d860f-122">If not specified will be generated.</span></span>

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

### <span data-ttu-id="d860f-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="d860f-123">-LocationData</span></span>
<span data-ttu-id="d860f-124">Gateway-plats.</span><span class="sxs-lookup"><span data-stu-id="d860f-124">Gateway location.</span></span>
<span data-ttu-id="d860f-125">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d860f-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d860f-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d860f-126">-Confirm</span></span>
<span data-ttu-id="d860f-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d860f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d860f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d860f-128">-WhatIf</span></span>
<span data-ttu-id="d860f-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d860f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d860f-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d860f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d860f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d860f-131">CommonParameters</span></span>
<span data-ttu-id="d860f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d860f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d860f-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d860f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d860f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d860f-134">INPUTS</span></span>

### <span data-ttu-id="d860f-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d860f-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d860f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d860f-136">System.String</span></span>

### <span data-ttu-id="d860f-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="d860f-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="d860f-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d860f-138">OUTPUTS</span></span>

### <span data-ttu-id="d860f-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="d860f-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="d860f-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d860f-140">NOTES</span></span>

## <span data-ttu-id="d860f-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d860f-141">RELATED LINKS</span></span>
