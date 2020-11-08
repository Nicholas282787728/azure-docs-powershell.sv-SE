---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 4bceb472fb3971b177f53b43fc48ad00c1422b58
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091907"
---
# <span data-ttu-id="2db6f-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2db6f-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="2db6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2db6f-102">SYNOPSIS</span></span>
<span data-ttu-id="2db6f-103">Ändrar en OpenID Connect-leverantör.</span><span class="sxs-lookup"><span data-stu-id="2db6f-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="2db6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2db6f-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2db6f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2db6f-105">DESCRIPTION</span></span>
<span data-ttu-id="2db6f-106">Cmdleten **set-AzApiManagementOpenIdConnectProvider** ändrar en OpenID Connect-leverantör i Azure API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="2db6f-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="2db6f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2db6f-107">EXAMPLES</span></span>

### <span data-ttu-id="2db6f-108">Exempel 1: ändra klient hemligheten för en leverantör</span><span class="sxs-lookup"><span data-stu-id="2db6f-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="2db6f-109">Det här kommandot ändrar den provider som har ID-OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="2db6f-109">This command modifies the provider that has the ID OICProvider01.</span></span>
<span data-ttu-id="2db6f-110">Kommandot anger en klient hemlighet för leverantören.</span><span class="sxs-lookup"><span data-stu-id="2db6f-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="2db6f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2db6f-111">PARAMETERS</span></span>

### <span data-ttu-id="2db6f-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="2db6f-112">-ClientId</span></span>
<span data-ttu-id="2db6f-113">Anger klient-ID för Developer Console.</span><span class="sxs-lookup"><span data-stu-id="2db6f-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="2db6f-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="2db6f-114">-ClientSecret</span></span>
<span data-ttu-id="2db6f-115">Anger utvecklarens klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="2db6f-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="2db6f-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2db6f-116">-Context</span></span>
<span data-ttu-id="2db6f-117">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2db6f-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2db6f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db6f-118">-DefaultProfile</span></span>
<span data-ttu-id="2db6f-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2db6f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2db6f-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="2db6f-120">-Description</span></span>
<span data-ttu-id="2db6f-121">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="2db6f-121">Specifies a description.</span></span>

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

### <span data-ttu-id="2db6f-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="2db6f-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="2db6f-123">Anger en URI för metadata-slutpunkt för providern.</span><span class="sxs-lookup"><span data-stu-id="2db6f-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="2db6f-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="2db6f-124">-Name</span></span>
<span data-ttu-id="2db6f-125">Anger ett eget namn för leverantören.</span><span class="sxs-lookup"><span data-stu-id="2db6f-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="2db6f-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="2db6f-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="2db6f-127">Anger ett ID för den provider som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="2db6f-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="2db6f-128">Om du inte anger något ID skapar den här cmdleten en.</span><span class="sxs-lookup"><span data-stu-id="2db6f-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="2db6f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2db6f-129">-PassThru</span></span>
<span data-ttu-id="2db6f-130">Anger att denna cmdlet returnerar **PsApiManagementOpenIdConnectProvider** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="2db6f-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2db6f-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2db6f-131">-Confirm</span></span>
<span data-ttu-id="2db6f-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2db6f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2db6f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2db6f-133">-WhatIf</span></span>
<span data-ttu-id="2db6f-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2db6f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2db6f-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2db6f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2db6f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db6f-136">CommonParameters</span></span>
<span data-ttu-id="2db6f-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2db6f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db6f-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2db6f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db6f-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2db6f-139">INPUTS</span></span>

### <span data-ttu-id="2db6f-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2db6f-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2db6f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2db6f-141">System.String</span></span>

### <span data-ttu-id="2db6f-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2db6f-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2db6f-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2db6f-143">OUTPUTS</span></span>

### <span data-ttu-id="2db6f-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2db6f-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="2db6f-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2db6f-145">NOTES</span></span>

## <span data-ttu-id="2db6f-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2db6f-146">RELATED LINKS</span></span>

[<span data-ttu-id="2db6f-147">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2db6f-147">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="2db6f-148">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2db6f-148">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="2db6f-149">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2db6f-149">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


