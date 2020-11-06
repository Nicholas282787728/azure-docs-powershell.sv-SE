---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c914c49aeb4f2a763a09c5b513bcbe7809110b05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585191"
---
# <span data-ttu-id="92b89-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="92b89-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="92b89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92b89-102">SYNOPSIS</span></span>
<span data-ttu-id="92b89-103">Ändrar en OpenID Connect-leverantör.</span><span class="sxs-lookup"><span data-stu-id="92b89-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92b89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92b89-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92b89-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92b89-105">DESCRIPTION</span></span>
<span data-ttu-id="92b89-106">Cmdleten **set-AzureRmApiManagementOpenIdConnectProvider** ändrar en OpenID Connect-leverantör i Azure API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="92b89-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="92b89-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92b89-107">EXAMPLES</span></span>

### <span data-ttu-id="92b89-108">Exempel 1: ändra klient hemligheten för en leverantör</span><span class="sxs-lookup"><span data-stu-id="92b89-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="92b89-109">Det här kommandot ändrar den provider som har ID-OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="92b89-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="92b89-110">Kommandot anger en klient hemlighet för leverantören.</span><span class="sxs-lookup"><span data-stu-id="92b89-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="92b89-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92b89-111">PARAMETERS</span></span>

### <span data-ttu-id="92b89-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="92b89-112">-ClientId</span></span>
<span data-ttu-id="92b89-113">Anger klient-ID för Developer Console.</span><span class="sxs-lookup"><span data-stu-id="92b89-113">Specifies the client ID of the developer console.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b89-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="92b89-114">-ClientSecret</span></span>
<span data-ttu-id="92b89-115">Anger utvecklarens klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="92b89-115">Specifies the client secret of the developer console.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b89-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="92b89-116">-Context</span></span>
<span data-ttu-id="92b89-117">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="92b89-117">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b89-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b89-118">-DefaultProfile</span></span>
<span data-ttu-id="92b89-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92b89-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b89-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="92b89-120">-Description</span></span>
<span data-ttu-id="92b89-121">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="92b89-121">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b89-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="92b89-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="92b89-123">Anger en URI för metadata-slutpunkt för providern.</span><span class="sxs-lookup"><span data-stu-id="92b89-123">Specifies a metadata endpoint URI of the provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b89-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="92b89-124">-Name</span></span>
<span data-ttu-id="92b89-125">Anger ett eget namn för leverantören.</span><span class="sxs-lookup"><span data-stu-id="92b89-125">Specifies a friendly name for the provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b89-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="92b89-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="92b89-127">Anger ett ID för den provider som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="92b89-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="92b89-128">Om du inte anger något ID skapar den här cmdleten en.</span><span class="sxs-lookup"><span data-stu-id="92b89-128">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b89-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92b89-129">-PassThru</span></span>
<span data-ttu-id="92b89-130">Anger att denna cmdlet returnerar **PsApiManagementOpenIdConnectProvider** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="92b89-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b89-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b89-131">CommonParameters</span></span>
<span data-ttu-id="92b89-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92b89-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b89-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92b89-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b89-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92b89-134">INPUTS</span></span>

### <span data-ttu-id="92b89-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="92b89-135">None</span></span>
<span data-ttu-id="92b89-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="92b89-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="92b89-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92b89-137">OUTPUTS</span></span>

### <span data-ttu-id="92b89-138">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="92b89-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="92b89-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92b89-139">NOTES</span></span>

## <span data-ttu-id="92b89-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92b89-140">RELATED LINKS</span></span>

[<span data-ttu-id="92b89-141">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="92b89-141">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="92b89-142">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="92b89-142">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="92b89-143">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="92b89-143">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


