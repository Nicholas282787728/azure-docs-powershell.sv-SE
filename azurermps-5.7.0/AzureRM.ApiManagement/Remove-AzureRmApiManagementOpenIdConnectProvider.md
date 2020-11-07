---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ee1ac7cda19f2b37ac1313d30075aa9c620bbd54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583707"
---
# <span data-ttu-id="f3296-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f3296-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="f3296-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3296-102">SYNOPSIS</span></span>
<span data-ttu-id="f3296-103">Tar bort en OpenID Connect-leverantör.</span><span class="sxs-lookup"><span data-stu-id="f3296-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3296-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3296-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3296-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3296-105">DESCRIPTION</span></span>
<span data-ttu-id="f3296-106">Cmdleten **Remove-AzureRmApiManagementOpenIdConnectProvider** tar bort en OpenID Connect-leverantör för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="f3296-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="f3296-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3296-107">EXAMPLES</span></span>

### <span data-ttu-id="f3296-108">Exempel 1: ta bort en leverantör</span><span class="sxs-lookup"><span data-stu-id="f3296-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="f3296-109">Det här kommandot tar bort en Provider med ID-OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="f3296-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="f3296-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3296-110">PARAMETERS</span></span>

### <span data-ttu-id="f3296-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="f3296-111">-Context</span></span>
<span data-ttu-id="f3296-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f3296-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f3296-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3296-113">-DefaultProfile</span></span>
<span data-ttu-id="f3296-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f3296-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f3296-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="f3296-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="f3296-116">Anger ett ID för den provider som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="f3296-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f3296-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3296-117">-PassThru</span></span>
<span data-ttu-id="f3296-118">Anger att denna cmdlet returnerar ett värde för $True om åtgärden lyckas eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="f3296-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="f3296-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f3296-119">-Confirm</span></span>
<span data-ttu-id="f3296-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3296-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3296-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3296-121">-WhatIf</span></span>
<span data-ttu-id="f3296-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f3296-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3296-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f3296-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3296-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3296-124">CommonParameters</span></span>
<span data-ttu-id="f3296-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3296-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3296-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3296-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3296-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3296-127">INPUTS</span></span>

### <span data-ttu-id="f3296-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="f3296-128">None</span></span>
<span data-ttu-id="f3296-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f3296-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3296-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3296-130">OUTPUTS</span></span>

### <span data-ttu-id="f3296-131">Returtyp</span><span class="sxs-lookup"><span data-stu-id="f3296-131">Boolean</span></span>

## <span data-ttu-id="f3296-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3296-132">NOTES</span></span>

## <span data-ttu-id="f3296-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3296-133">RELATED LINKS</span></span>

[<span data-ttu-id="f3296-134">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f3296-134">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f3296-135">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f3296-135">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f3296-136">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f3296-136">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)

