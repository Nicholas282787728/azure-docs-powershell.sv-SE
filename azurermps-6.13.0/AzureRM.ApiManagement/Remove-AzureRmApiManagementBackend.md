---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: ef00a5140dc25065c05494211721c5773a9b5243
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573064"
---
# <span data-ttu-id="d9743-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d9743-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="d9743-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9743-102">SYNOPSIS</span></span>
<span data-ttu-id="d9743-103">Tar bort en server del.</span><span class="sxs-lookup"><span data-stu-id="d9743-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9743-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9743-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9743-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9743-105">DESCRIPTION</span></span>
<span data-ttu-id="d9743-106">Tar bort en server del som anges av identifieraren från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="d9743-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="d9743-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9743-107">EXAMPLES</span></span>

### <span data-ttu-id="d9743-108">Exempel 1: ta bort Server delen 123</span><span class="sxs-lookup"><span data-stu-id="d9743-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="d9743-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9743-109">PARAMETERS</span></span>

### <span data-ttu-id="d9743-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="d9743-110">-BackendId</span></span>
<span data-ttu-id="d9743-111">Identifierare för befintlig server del.</span><span class="sxs-lookup"><span data-stu-id="d9743-111">Identifier of existing backend.</span></span>
<span data-ttu-id="d9743-112">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d9743-112">This parameter is required.</span></span>

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

### <span data-ttu-id="d9743-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d9743-113">-Context</span></span>
<span data-ttu-id="d9743-114">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d9743-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d9743-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d9743-115">This parameter is required.</span></span>

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

### <span data-ttu-id="d9743-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9743-116">-DefaultProfile</span></span>
<span data-ttu-id="d9743-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9743-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9743-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9743-118">-PassThru</span></span>
<span data-ttu-id="d9743-119">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="d9743-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d9743-120">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d9743-120">This parameter is optional.</span></span>
<span data-ttu-id="d9743-121">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="d9743-121">Default value is false.</span></span>

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

### <span data-ttu-id="d9743-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d9743-122">-Confirm</span></span>
<span data-ttu-id="d9743-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d9743-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9743-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9743-124">-WhatIf</span></span>
<span data-ttu-id="d9743-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d9743-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9743-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d9743-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9743-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9743-127">CommonParameters</span></span>
<span data-ttu-id="d9743-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9743-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9743-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9743-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9743-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9743-130">INPUTS</span></span>

### <span data-ttu-id="d9743-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d9743-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d9743-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d9743-132">System.String</span></span>

### <span data-ttu-id="d9743-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d9743-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d9743-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9743-134">OUTPUTS</span></span>

### <span data-ttu-id="d9743-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9743-135">System.Boolean</span></span>

## <span data-ttu-id="d9743-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9743-136">NOTES</span></span>

## <span data-ttu-id="d9743-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9743-137">RELATED LINKS</span></span>

[<span data-ttu-id="d9743-138">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d9743-138">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="d9743-139">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d9743-139">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="d9743-140">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d9743-140">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="d9743-141">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d9743-141">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="d9743-142">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d9743-142">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
