---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f890236907ea0a717245d9345be276a6ccf04b8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579843"
---
# <span data-ttu-id="bdec3-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bdec3-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="bdec3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bdec3-102">SYNOPSIS</span></span>
<span data-ttu-id="bdec3-103">Ändrar en OpenID Connect-leverantör.</span><span class="sxs-lookup"><span data-stu-id="bdec3-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdec3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bdec3-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdec3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bdec3-105">DESCRIPTION</span></span>
<span data-ttu-id="bdec3-106">Cmdleten **set-AzureRmApiManagementOpenIdConnectProvider** ändrar en OpenID Connect-leverantör i Azure API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="bdec3-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="bdec3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bdec3-107">EXAMPLES</span></span>

### <span data-ttu-id="bdec3-108">Exempel 1: ändra klient hemligheten för en leverantör</span><span class="sxs-lookup"><span data-stu-id="bdec3-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="bdec3-109">Det här kommandot ändrar den provider som har ID-OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="bdec3-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="bdec3-110">Kommandot anger en klient hemlighet för leverantören.</span><span class="sxs-lookup"><span data-stu-id="bdec3-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="bdec3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bdec3-111">PARAMETERS</span></span>

### <span data-ttu-id="bdec3-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="bdec3-112">-ClientId</span></span>
<span data-ttu-id="bdec3-113">Anger klient-ID för Developer Console.</span><span class="sxs-lookup"><span data-stu-id="bdec3-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="bdec3-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="bdec3-114">-ClientSecret</span></span>
<span data-ttu-id="bdec3-115">Anger utvecklarens klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="bdec3-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="bdec3-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="bdec3-116">-Context</span></span>
<span data-ttu-id="bdec3-117">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bdec3-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bdec3-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="bdec3-118">-Description</span></span>
<span data-ttu-id="bdec3-119">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="bdec3-119">Specifies a description.</span></span>

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

### <span data-ttu-id="bdec3-120">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="bdec3-120">-MetadataEndpointUri</span></span>
<span data-ttu-id="bdec3-121">Anger en URI för metadata-slutpunkt för providern.</span><span class="sxs-lookup"><span data-stu-id="bdec3-121">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="bdec3-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="bdec3-122">-Name</span></span>
<span data-ttu-id="bdec3-123">Anger ett eget namn för leverantören.</span><span class="sxs-lookup"><span data-stu-id="bdec3-123">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="bdec3-124">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="bdec3-124">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="bdec3-125">Anger ett ID för den provider som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="bdec3-125">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="bdec3-126">Om du inte anger något ID skapar den här cmdleten en.</span><span class="sxs-lookup"><span data-stu-id="bdec3-126">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="bdec3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdec3-127">-PassThru</span></span>
<span data-ttu-id="bdec3-128">Anger att denna cmdlet returnerar **PsApiManagementOpenIdConnectProvider** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="bdec3-128">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bdec3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdec3-129">-DefaultProfile</span></span>
<span data-ttu-id="bdec3-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bdec3-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdec3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdec3-131">CommonParameters</span></span>
<span data-ttu-id="bdec3-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdec3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdec3-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdec3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdec3-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bdec3-134">INPUTS</span></span>

## <span data-ttu-id="bdec3-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bdec3-135">OUTPUTS</span></span>

### <span data-ttu-id="bdec3-136">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bdec3-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="bdec3-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bdec3-137">NOTES</span></span>

## <span data-ttu-id="bdec3-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bdec3-138">RELATED LINKS</span></span>

[<span data-ttu-id="bdec3-139">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bdec3-139">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bdec3-140">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bdec3-140">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bdec3-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bdec3-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


