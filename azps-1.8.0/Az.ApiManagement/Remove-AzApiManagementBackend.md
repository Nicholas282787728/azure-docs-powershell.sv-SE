---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 3a725bf8dedec948277fac69be029375c3ab91a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754898"
---
# <span data-ttu-id="55580-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="55580-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="55580-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55580-102">SYNOPSIS</span></span>
<span data-ttu-id="55580-103">Tar bort en server del.</span><span class="sxs-lookup"><span data-stu-id="55580-103">Removes a Backend.</span></span>

## <span data-ttu-id="55580-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55580-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55580-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55580-105">DESCRIPTION</span></span>
<span data-ttu-id="55580-106">Tar bort en server del som anges av identifieraren från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="55580-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="55580-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55580-107">EXAMPLES</span></span>

### <span data-ttu-id="55580-108">Exempel 1: ta bort Server delen 123</span><span class="sxs-lookup"><span data-stu-id="55580-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="55580-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55580-109">PARAMETERS</span></span>

### <span data-ttu-id="55580-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="55580-110">-BackendId</span></span>
<span data-ttu-id="55580-111">Identifierare för befintlig server del.</span><span class="sxs-lookup"><span data-stu-id="55580-111">Identifier of existing backend.</span></span>
<span data-ttu-id="55580-112">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="55580-112">This parameter is required.</span></span>

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

### <span data-ttu-id="55580-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="55580-113">-Context</span></span>
<span data-ttu-id="55580-114">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="55580-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="55580-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="55580-115">This parameter is required.</span></span>

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

### <span data-ttu-id="55580-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55580-116">-DefaultProfile</span></span>
<span data-ttu-id="55580-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55580-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55580-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55580-118">-PassThru</span></span>
<span data-ttu-id="55580-119">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="55580-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="55580-120">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="55580-120">This parameter is optional.</span></span>
<span data-ttu-id="55580-121">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="55580-121">Default value is false.</span></span>

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

### <span data-ttu-id="55580-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="55580-122">-Confirm</span></span>
<span data-ttu-id="55580-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="55580-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55580-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55580-124">-WhatIf</span></span>
<span data-ttu-id="55580-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="55580-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55580-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="55580-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55580-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55580-127">CommonParameters</span></span>
<span data-ttu-id="55580-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55580-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55580-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55580-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55580-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55580-130">INPUTS</span></span>

### <span data-ttu-id="55580-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="55580-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="55580-132">System. String</span><span class="sxs-lookup"><span data-stu-id="55580-132">System.String</span></span>

### <span data-ttu-id="55580-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55580-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="55580-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55580-134">OUTPUTS</span></span>

### <span data-ttu-id="55580-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55580-135">System.Boolean</span></span>

## <span data-ttu-id="55580-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55580-136">NOTES</span></span>

## <span data-ttu-id="55580-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55580-137">RELATED LINKS</span></span>

[<span data-ttu-id="55580-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="55580-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="55580-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="55580-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="55580-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="55580-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="55580-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="55580-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="55580-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="55580-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
