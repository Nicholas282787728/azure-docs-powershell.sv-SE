---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: 40c8229f1a14144516c465ef56908c3dd1fb9bc1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917758"
---
# <span data-ttu-id="95d8d-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95d8d-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="95d8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="95d8d-103">Tar bort API-hanteringskonsolen från ett angivet scope.</span><span class="sxs-lookup"><span data-stu-id="95d8d-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="95d8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95d8d-104">SYNTAX</span></span>

### <span data-ttu-id="95d8d-105">RemoveTenantLevel (standard)</span><span class="sxs-lookup"><span data-stu-id="95d8d-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95d8d-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="95d8d-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95d8d-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="95d8d-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95d8d-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="95d8d-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95d8d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95d8d-109">DESCRIPTION</span></span>
<span data-ttu-id="95d8d-110">Cmdleten **Remove-AzApiManagementPolicy** tar bort API-hanterings principen från angivet scope.</span><span class="sxs-lookup"><span data-stu-id="95d8d-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="95d8d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95d8d-111">EXAMPLES</span></span>

### <span data-ttu-id="95d8d-112">Exempel 1: ta bort principen för klient organisations nivå</span><span class="sxs-lookup"><span data-stu-id="95d8d-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="95d8d-113">Det här kommandot tar bort policyn för klient organisations nivå från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="95d8d-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="95d8d-114">Exempel 2: ta bort produktens policy princip</span><span class="sxs-lookup"><span data-stu-id="95d8d-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="95d8d-115">Det här kommandot tar bort produktens princip från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="95d8d-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="95d8d-116">Exempel 3: ta bort API-scope-principen</span><span class="sxs-lookup"><span data-stu-id="95d8d-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="95d8d-117">Det här kommandot tar bort API-scope-principen från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="95d8d-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="95d8d-118">Exempel 4: ta bort åtgärdens scope-princip</span><span class="sxs-lookup"><span data-stu-id="95d8d-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="95d8d-119">Det här kommandot tar bort åtgärdens omfattning från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="95d8d-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="95d8d-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95d8d-120">PARAMETERS</span></span>

### <span data-ttu-id="95d8d-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="95d8d-121">-ApiId</span></span>
<span data-ttu-id="95d8d-122">Anger ID för ett befintligt API.</span><span class="sxs-lookup"><span data-stu-id="95d8d-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="95d8d-123">Om du anger den här parametern tar cmdleten bort API-scope-principen.</span><span class="sxs-lookup"><span data-stu-id="95d8d-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveApiLevel, RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d8d-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="95d8d-124">-Context</span></span>
<span data-ttu-id="95d8d-125">Anger instansen för **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="95d8d-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="95d8d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d8d-126">-DefaultProfile</span></span>
<span data-ttu-id="95d8d-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95d8d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95d8d-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="95d8d-128">-OperationId</span></span>
<span data-ttu-id="95d8d-129">Anger identifierare för en befintlig åtgärd.</span><span class="sxs-lookup"><span data-stu-id="95d8d-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="95d8d-130">Om du anger den här parametern med parametern *ApiId* tar denna cmdlet bort åtgärdens scope-princip.</span><span class="sxs-lookup"><span data-stu-id="95d8d-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d8d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95d8d-131">-PassThru</span></span>
<span data-ttu-id="95d8d-132">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="95d8d-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="95d8d-133">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="95d8d-133">-ProductId</span></span>
<span data-ttu-id="95d8d-134">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="95d8d-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="95d8d-135">Om du anger den här parametern tas produktens princip bort med cmdleten.</span><span class="sxs-lookup"><span data-stu-id="95d8d-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d8d-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="95d8d-136">-Confirm</span></span>
<span data-ttu-id="95d8d-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="95d8d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95d8d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d8d-138">-WhatIf</span></span>
<span data-ttu-id="95d8d-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="95d8d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95d8d-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="95d8d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95d8d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d8d-141">CommonParameters</span></span>
<span data-ttu-id="95d8d-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d8d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d8d-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95d8d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d8d-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95d8d-144">INPUTS</span></span>

### <span data-ttu-id="95d8d-145">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="95d8d-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="95d8d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="95d8d-146">System.String</span></span>

### <span data-ttu-id="95d8d-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="95d8d-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="95d8d-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95d8d-148">OUTPUTS</span></span>

### <span data-ttu-id="95d8d-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95d8d-149">System.Boolean</span></span>

## <span data-ttu-id="95d8d-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95d8d-150">NOTES</span></span>

## <span data-ttu-id="95d8d-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95d8d-151">RELATED LINKS</span></span>

[<span data-ttu-id="95d8d-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95d8d-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="95d8d-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="95d8d-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


