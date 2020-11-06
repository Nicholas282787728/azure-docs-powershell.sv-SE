---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d8cc54570b1282889a93c803e1216096cde35b27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573035"
---
# <span data-ttu-id="dbe43-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="dbe43-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="dbe43-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dbe43-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe43-103">Tar bort en befintlig identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dbe43-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbe43-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dbe43-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbe43-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dbe43-105">DESCRIPTION</span></span>
<span data-ttu-id="dbe43-106">Tar bort en befintlig identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dbe43-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="dbe43-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dbe43-107">EXAMPLES</span></span>

### <span data-ttu-id="dbe43-108">Tar bort inställningarna för Facebook-identitetsprovider från ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="dbe43-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="dbe43-109">Tar bort konfiguration som är relaterad till Facebook Identity Provider-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dbe43-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="dbe43-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dbe43-110">PARAMETERS</span></span>

### <span data-ttu-id="dbe43-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="dbe43-111">-Context</span></span>
<span data-ttu-id="dbe43-112">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="dbe43-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dbe43-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="dbe43-113">This parameter is required.</span></span>

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

### <span data-ttu-id="dbe43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe43-114">-DefaultProfile</span></span>
<span data-ttu-id="dbe43-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dbe43-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbe43-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbe43-116">-PassThru</span></span>
<span data-ttu-id="dbe43-117">Anger att denna cmdlet returnerar ett värde för $True om åtgärden lyckas eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="dbe43-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="dbe43-118">– Skriv</span><span class="sxs-lookup"><span data-stu-id="dbe43-118">-Type</span></span>
<span data-ttu-id="dbe43-119">Identifierare för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="dbe43-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="dbe43-120">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="dbe43-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbe43-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dbe43-121">-Confirm</span></span>
<span data-ttu-id="dbe43-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dbe43-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbe43-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbe43-123">-WhatIf</span></span>
<span data-ttu-id="dbe43-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dbe43-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbe43-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dbe43-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbe43-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe43-126">CommonParameters</span></span>
<span data-ttu-id="dbe43-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbe43-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe43-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbe43-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe43-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dbe43-129">INPUTS</span></span>

### <span data-ttu-id="dbe43-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dbe43-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dbe43-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="dbe43-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="dbe43-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dbe43-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dbe43-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dbe43-133">OUTPUTS</span></span>

### <span data-ttu-id="dbe43-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dbe43-134">System.Boolean</span></span>

## <span data-ttu-id="dbe43-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dbe43-135">NOTES</span></span>

## <span data-ttu-id="dbe43-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dbe43-136">RELATED LINKS</span></span>

[<span data-ttu-id="dbe43-137">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="dbe43-137">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="dbe43-138">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="dbe43-138">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="dbe43-139">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="dbe43-139">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

