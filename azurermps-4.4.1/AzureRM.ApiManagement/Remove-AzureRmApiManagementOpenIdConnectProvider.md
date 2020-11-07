---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 686b988ef5bf62e5eed7e4f8fae94f6b29b1b4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575048"
---
# <span data-ttu-id="b68b2-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b68b2-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b68b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b68b2-102">SYNOPSIS</span></span>
<span data-ttu-id="b68b2-103">Tar bort en OpenID Connect-leverantör.</span><span class="sxs-lookup"><span data-stu-id="b68b2-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b68b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b68b2-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b68b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b68b2-105">DESCRIPTION</span></span>
<span data-ttu-id="b68b2-106">Cmdleten **Remove-AzureRmApiManagementOpenIdConnectProvider** tar bort en OpenID Connect-leverantör för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="b68b2-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="b68b2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b68b2-107">EXAMPLES</span></span>

### <span data-ttu-id="b68b2-108">Exempel 1: ta bort en leverantör</span><span class="sxs-lookup"><span data-stu-id="b68b2-108">Example 1: Remove a provider</span></span>
```
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="b68b2-109">Det här kommandot tar bort en Provider med ID-OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="b68b2-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="b68b2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b68b2-110">PARAMETERS</span></span>

### <span data-ttu-id="b68b2-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b68b2-111">-Context</span></span>
<span data-ttu-id="b68b2-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b68b2-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b68b2-113">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="b68b2-113">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="b68b2-114">Anger ett ID för den provider som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="b68b2-114">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b68b2-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b68b2-115">-PassThru</span></span>
<span data-ttu-id="b68b2-116">Anger att denna cmdlet returnerar ett värde för $True om åtgärden lyckas eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="b68b2-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="b68b2-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b68b2-117">-Confirm</span></span>
<span data-ttu-id="b68b2-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b68b2-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b68b2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b68b2-119">-WhatIf</span></span>
<span data-ttu-id="b68b2-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b68b2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b68b2-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b68b2-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b68b2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b68b2-122">-DefaultProfile</span></span>
<span data-ttu-id="b68b2-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b68b2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b68b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b68b2-124">CommonParameters</span></span>
<span data-ttu-id="b68b2-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b68b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b68b2-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b68b2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b68b2-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b68b2-127">INPUTS</span></span>

## <span data-ttu-id="b68b2-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b68b2-128">OUTPUTS</span></span>

### <span data-ttu-id="b68b2-129">Returtyp</span><span class="sxs-lookup"><span data-stu-id="b68b2-129">Boolean</span></span>

## <span data-ttu-id="b68b2-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b68b2-130">NOTES</span></span>

## <span data-ttu-id="b68b2-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b68b2-131">RELATED LINKS</span></span>

[<span data-ttu-id="b68b2-132">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b68b2-132">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b68b2-133">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b68b2-133">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b68b2-134">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b68b2-134">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)

