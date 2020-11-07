---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: fe320af601fad9d905471525b1a418c12c355f63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917685"
---
# <span data-ttu-id="9854a-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="9854a-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="9854a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9854a-102">SYNOPSIS</span></span>
<span data-ttu-id="9854a-103">Ändrar en OpenID Connect-leverantör.</span><span class="sxs-lookup"><span data-stu-id="9854a-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="9854a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9854a-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9854a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9854a-105">DESCRIPTION</span></span>
<span data-ttu-id="9854a-106">Cmdleten **set-AzApiManagementOpenIdConnectProvider** ändrar en OpenID Connect-leverantör i Azure API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="9854a-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="9854a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9854a-107">EXAMPLES</span></span>

### <span data-ttu-id="9854a-108">Exempel 1: ändra klient hemligheten för en leverantör</span><span class="sxs-lookup"><span data-stu-id="9854a-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="9854a-109">Det här kommandot ändrar den provider som har ID-OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="9854a-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="9854a-110">Kommandot anger en klient hemlighet för leverantören.</span><span class="sxs-lookup"><span data-stu-id="9854a-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="9854a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9854a-111">PARAMETERS</span></span>

### <span data-ttu-id="9854a-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="9854a-112">-ClientId</span></span>
<span data-ttu-id="9854a-113">Anger klient-ID för Developer Console.</span><span class="sxs-lookup"><span data-stu-id="9854a-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="9854a-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="9854a-114">-ClientSecret</span></span>
<span data-ttu-id="9854a-115">Anger utvecklarens klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="9854a-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="9854a-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="9854a-116">-Context</span></span>
<span data-ttu-id="9854a-117">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9854a-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9854a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9854a-118">-DefaultProfile</span></span>
<span data-ttu-id="9854a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9854a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9854a-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="9854a-120">-Description</span></span>
<span data-ttu-id="9854a-121">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="9854a-121">Specifies a description.</span></span>

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

### <span data-ttu-id="9854a-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="9854a-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="9854a-123">Anger en URI för metadata-slutpunkt för providern.</span><span class="sxs-lookup"><span data-stu-id="9854a-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="9854a-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="9854a-124">-Name</span></span>
<span data-ttu-id="9854a-125">Anger ett eget namn för leverantören.</span><span class="sxs-lookup"><span data-stu-id="9854a-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="9854a-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="9854a-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="9854a-127">Anger ett ID för den provider som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="9854a-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="9854a-128">Om du inte anger något ID skapar den här cmdleten en.</span><span class="sxs-lookup"><span data-stu-id="9854a-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="9854a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9854a-129">-PassThru</span></span>
<span data-ttu-id="9854a-130">Anger att denna cmdlet returnerar **PsApiManagementOpenIdConnectProvider** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="9854a-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9854a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9854a-131">CommonParameters</span></span>
<span data-ttu-id="9854a-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9854a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9854a-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9854a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9854a-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9854a-134">INPUTS</span></span>

### <span data-ttu-id="9854a-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9854a-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9854a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9854a-136">System.String</span></span>

### <span data-ttu-id="9854a-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9854a-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9854a-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9854a-138">OUTPUTS</span></span>

### <span data-ttu-id="9854a-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="9854a-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="9854a-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9854a-140">NOTES</span></span>

## <span data-ttu-id="9854a-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9854a-141">RELATED LINKS</span></span>

[<span data-ttu-id="9854a-142">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="9854a-142">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="9854a-143">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="9854a-143">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="9854a-144">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="9854a-144">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


