---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 03f56a17d038407b3a33c09188c9a29b6f4caf09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575057"
---
# <span data-ttu-id="49fe2-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="49fe2-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="49fe2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="49fe2-103">Tar bort en server del.</span><span class="sxs-lookup"><span data-stu-id="49fe2-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49fe2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49fe2-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49fe2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49fe2-105">DESCRIPTION</span></span>
<span data-ttu-id="49fe2-106">Tar bort en server del som anges av identifieraren från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="49fe2-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="49fe2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49fe2-107">EXAMPLES</span></span>

### <span data-ttu-id="49fe2-108">Exempel 1: ta bort Server delen 123</span><span class="sxs-lookup"><span data-stu-id="49fe2-108">Example 1: Remove the Backend 123</span></span>
```
Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="49fe2-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49fe2-109">PARAMETERS</span></span>

### <span data-ttu-id="49fe2-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="49fe2-110">-BackendId</span></span>
<span data-ttu-id="49fe2-111">Identifierare för befintlig server del.</span><span class="sxs-lookup"><span data-stu-id="49fe2-111">Identifier of existing backend.</span></span>
<span data-ttu-id="49fe2-112">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="49fe2-112">This parameter is required.</span></span>

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

### <span data-ttu-id="49fe2-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="49fe2-113">-Context</span></span>
<span data-ttu-id="49fe2-114">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="49fe2-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="49fe2-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="49fe2-115">This parameter is required.</span></span>

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

### <span data-ttu-id="49fe2-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49fe2-116">-PassThru</span></span>
<span data-ttu-id="49fe2-117">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="49fe2-117">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="49fe2-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="49fe2-118">This parameter is optional.</span></span>
<span data-ttu-id="49fe2-119">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="49fe2-119">Default value is false.</span></span>

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

### <span data-ttu-id="49fe2-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="49fe2-120">-Confirm</span></span>
<span data-ttu-id="49fe2-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="49fe2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49fe2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49fe2-122">-WhatIf</span></span>
<span data-ttu-id="49fe2-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="49fe2-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49fe2-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="49fe2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49fe2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49fe2-125">-DefaultProfile</span></span>
<span data-ttu-id="49fe2-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="49fe2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49fe2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49fe2-127">CommonParameters</span></span>
<span data-ttu-id="49fe2-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49fe2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49fe2-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49fe2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49fe2-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49fe2-130">INPUTS</span></span>

## <span data-ttu-id="49fe2-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49fe2-131">OUTPUTS</span></span>

### <span data-ttu-id="49fe2-132">bool</span><span class="sxs-lookup"><span data-stu-id="49fe2-132">bool</span></span>

## <span data-ttu-id="49fe2-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49fe2-133">NOTES</span></span>

## <span data-ttu-id="49fe2-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49fe2-134">RELATED LINKS</span></span>

[<span data-ttu-id="49fe2-135">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="49fe2-135">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="49fe2-136">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="49fe2-136">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="49fe2-137">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="49fe2-137">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="49fe2-138">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="49fe2-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="49fe2-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="49fe2-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
