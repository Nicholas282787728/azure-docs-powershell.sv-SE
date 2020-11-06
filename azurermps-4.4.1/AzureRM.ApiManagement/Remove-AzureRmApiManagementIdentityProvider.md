---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: ecbb2b6671f1482f31cb7b3f0b07d4e9be4bbb3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575053"
---
# <span data-ttu-id="716bf-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="716bf-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="716bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="716bf-102">SYNOPSIS</span></span>
<span data-ttu-id="716bf-103">Tar bort en befintlig identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="716bf-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="716bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="716bf-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="716bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="716bf-105">DESCRIPTION</span></span>
<span data-ttu-id="716bf-106">Tar bort en befintlig identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="716bf-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="716bf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="716bf-107">EXAMPLES</span></span>

### <span data-ttu-id="716bf-108">Tar bort inställningarna för Facebook-identitetsprovider från ApiManagement-tjänsten</span><span class="sxs-lookup"><span data-stu-id="716bf-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="716bf-109">Tar bort konfiguration som är relaterad till Facebook Identity Provider-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="716bf-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="716bf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="716bf-110">PARAMETERS</span></span>

### <span data-ttu-id="716bf-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="716bf-111">-Context</span></span>
<span data-ttu-id="716bf-112">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="716bf-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="716bf-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="716bf-113">This parameter is required.</span></span>

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

### <span data-ttu-id="716bf-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="716bf-114">-PassThru</span></span>
<span data-ttu-id="716bf-115">Anger att denna cmdlet returnerar ett värde för $True om åtgärden lyckas eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="716bf-115">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


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

### <span data-ttu-id="716bf-116">– Skriv</span><span class="sxs-lookup"><span data-stu-id="716bf-116">-Type</span></span>
<span data-ttu-id="716bf-117">Identifierare för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="716bf-117">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="716bf-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="716bf-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="716bf-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="716bf-119">-Confirm</span></span>
<span data-ttu-id="716bf-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="716bf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="716bf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="716bf-121">-WhatIf</span></span>
<span data-ttu-id="716bf-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="716bf-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="716bf-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="716bf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="716bf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716bf-124">-DefaultProfile</span></span>
<span data-ttu-id="716bf-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="716bf-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="716bf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716bf-126">CommonParameters</span></span>
<span data-ttu-id="716bf-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="716bf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="716bf-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="716bf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716bf-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="716bf-129">INPUTS</span></span>

## <span data-ttu-id="716bf-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="716bf-130">OUTPUTS</span></span>

### <span data-ttu-id="716bf-131">bool</span><span class="sxs-lookup"><span data-stu-id="716bf-131">bool</span></span>

## <span data-ttu-id="716bf-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="716bf-132">NOTES</span></span>

## <span data-ttu-id="716bf-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="716bf-133">RELATED LINKS</span></span>

[<span data-ttu-id="716bf-134">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="716bf-134">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="716bf-135">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="716bf-135">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="716bf-136">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="716bf-136">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

