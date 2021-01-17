---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: e15e6757d6a4d0f6e84a9580877deecdeede94ee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411560"
---
# <span data-ttu-id="c1621-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c1621-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="c1621-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1621-102">SYNOPSIS</span></span>
<span data-ttu-id="c1621-103">Tar bort en befintlig identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c1621-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="c1621-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1621-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1621-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1621-105">DESCRIPTION</span></span>
<span data-ttu-id="c1621-106">Tar bort en befintlig identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c1621-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="c1621-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1621-107">EXAMPLES</span></span>

### <span data-ttu-id="c1621-108">Exempel 1: tar bort Facebook-identitetsmappen från ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="c1621-108">Example 1: Removes the Facebook identity provider settings from ApiManagement service</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="c1621-109">Tar bort konfiguration som är relaterad till Facebook Identity Provider-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c1621-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="c1621-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1621-110">PARAMETERS</span></span>

### <span data-ttu-id="c1621-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c1621-111">-Context</span></span>
<span data-ttu-id="c1621-112">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c1621-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c1621-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c1621-113">This parameter is required.</span></span>

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

### <span data-ttu-id="c1621-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1621-114">-DefaultProfile</span></span>
<span data-ttu-id="c1621-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1621-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1621-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1621-116">-PassThru</span></span>
<span data-ttu-id="c1621-117">Anger att denna cmdlet returnerar ett värde för $True om åtgärden lyckas eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="c1621-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="c1621-118">– Skriv</span><span class="sxs-lookup"><span data-stu-id="c1621-118">-Type</span></span>
<span data-ttu-id="c1621-119">Identifierare för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="c1621-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="c1621-120">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c1621-120">This parameter is required.</span></span>

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

### <span data-ttu-id="c1621-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c1621-121">-Confirm</span></span>
<span data-ttu-id="c1621-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c1621-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1621-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1621-123">-WhatIf</span></span>
<span data-ttu-id="c1621-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c1621-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1621-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c1621-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1621-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1621-126">CommonParameters</span></span>
<span data-ttu-id="c1621-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1621-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1621-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1621-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1621-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1621-129">INPUTS</span></span>

### <span data-ttu-id="c1621-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c1621-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c1621-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="c1621-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="c1621-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c1621-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c1621-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1621-133">OUTPUTS</span></span>

### <span data-ttu-id="c1621-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1621-134">System.Boolean</span></span>

## <span data-ttu-id="c1621-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1621-135">NOTES</span></span>

## <span data-ttu-id="c1621-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1621-136">RELATED LINKS</span></span>

[<span data-ttu-id="c1621-137">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c1621-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="c1621-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c1621-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="c1621-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c1621-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

