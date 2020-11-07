---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: c4f2ce8db3a799ad3d49d1c967da93a8fea93a39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745703"
---
# <span data-ttu-id="63a08-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="63a08-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="63a08-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63a08-102">SYNOPSIS</span></span>
<span data-ttu-id="63a08-103">Tar bort API-hanteringskonsolen från ett angivet scope.</span><span class="sxs-lookup"><span data-stu-id="63a08-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="63a08-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63a08-104">SYNTAX</span></span>

### <span data-ttu-id="63a08-105">RemoveTenantLevel (standard)</span><span class="sxs-lookup"><span data-stu-id="63a08-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63a08-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="63a08-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63a08-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="63a08-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63a08-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="63a08-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63a08-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63a08-109">DESCRIPTION</span></span>
<span data-ttu-id="63a08-110">Cmdleten **Remove-AzApiManagementPolicy** tar bort API-hanterings principen från angivet scope.</span><span class="sxs-lookup"><span data-stu-id="63a08-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="63a08-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63a08-111">EXAMPLES</span></span>

### <span data-ttu-id="63a08-112">Exempel 1: ta bort principen för klient organisations nivå</span><span class="sxs-lookup"><span data-stu-id="63a08-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="63a08-113">Det här kommandot tar bort policyn för klient organisations nivå från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="63a08-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="63a08-114">Exempel 2: ta bort produktens policy princip</span><span class="sxs-lookup"><span data-stu-id="63a08-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="63a08-115">Det här kommandot tar bort produktens princip från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="63a08-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="63a08-116">Exempel 3: ta bort API-scope-principen</span><span class="sxs-lookup"><span data-stu-id="63a08-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="63a08-117">Det här kommandot tar bort API-scope-principen från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="63a08-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="63a08-118">Exempel 4: ta bort åtgärdens scope-princip</span><span class="sxs-lookup"><span data-stu-id="63a08-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="63a08-119">Det här kommandot tar bort åtgärdens omfattning från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="63a08-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="63a08-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63a08-120">PARAMETERS</span></span>

### <span data-ttu-id="63a08-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="63a08-121">-ApiId</span></span>
<span data-ttu-id="63a08-122">Anger ID för ett befintligt API.</span><span class="sxs-lookup"><span data-stu-id="63a08-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="63a08-123">Om du anger den här parametern tar cmdleten bort API-scope-principen.</span><span class="sxs-lookup"><span data-stu-id="63a08-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="63a08-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="63a08-124">-Context</span></span>
<span data-ttu-id="63a08-125">Anger instansen för **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="63a08-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="63a08-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a08-126">-DefaultProfile</span></span>
<span data-ttu-id="63a08-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63a08-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63a08-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="63a08-128">-OperationId</span></span>
<span data-ttu-id="63a08-129">Anger identifierare för en befintlig åtgärd.</span><span class="sxs-lookup"><span data-stu-id="63a08-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="63a08-130">Om du anger den här parametern med parametern *ApiId* tar denna cmdlet bort åtgärdens scope-princip.</span><span class="sxs-lookup"><span data-stu-id="63a08-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="63a08-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63a08-131">-PassThru</span></span>
<span data-ttu-id="63a08-132">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="63a08-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="63a08-133">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="63a08-133">-ProductId</span></span>
<span data-ttu-id="63a08-134">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="63a08-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="63a08-135">Om du anger den här parametern tas produktens princip bort med cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63a08-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="63a08-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63a08-136">-Confirm</span></span>
<span data-ttu-id="63a08-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63a08-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63a08-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63a08-138">-WhatIf</span></span>
<span data-ttu-id="63a08-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63a08-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63a08-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63a08-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63a08-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a08-141">CommonParameters</span></span>
<span data-ttu-id="63a08-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63a08-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a08-143">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63a08-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a08-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63a08-144">INPUTS</span></span>

### <span data-ttu-id="63a08-145">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="63a08-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="63a08-146">System. String</span><span class="sxs-lookup"><span data-stu-id="63a08-146">System.String</span></span>

### <span data-ttu-id="63a08-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="63a08-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="63a08-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63a08-148">OUTPUTS</span></span>

### <span data-ttu-id="63a08-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="63a08-149">System.Boolean</span></span>

## <span data-ttu-id="63a08-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63a08-150">NOTES</span></span>

## <span data-ttu-id="63a08-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63a08-151">RELATED LINKS</span></span>

[<span data-ttu-id="63a08-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="63a08-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="63a08-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="63a08-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


