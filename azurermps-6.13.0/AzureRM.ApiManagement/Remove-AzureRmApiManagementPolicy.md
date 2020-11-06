---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 1066598a9e255cecbf7238208b5f06f74d88511e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576350"
---
# <span data-ttu-id="333a9-101">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="333a9-101">Remove-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="333a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="333a9-102">SYNOPSIS</span></span>
<span data-ttu-id="333a9-103">Tar bort API-hanteringskonsolen från ett angivet scope.</span><span class="sxs-lookup"><span data-stu-id="333a9-103">Removes the API Management policy from a specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="333a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="333a9-104">SYNTAX</span></span>

### <span data-ttu-id="333a9-105">RemoveTenantLevel (standard)</span><span class="sxs-lookup"><span data-stu-id="333a9-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="333a9-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="333a9-106">RemoveProductLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="333a9-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="333a9-107">RemoveApiLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="333a9-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="333a9-108">RemoveOperationLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="333a9-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="333a9-109">DESCRIPTION</span></span>
<span data-ttu-id="333a9-110">Cmdleten **Remove-AzureRmApiManagementPolicy** tar bort API-hanterings principen från angivet scope.</span><span class="sxs-lookup"><span data-stu-id="333a9-110">The **Remove-AzureRmApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="333a9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="333a9-111">EXAMPLES</span></span>

### <span data-ttu-id="333a9-112">Exempel 1: ta bort principen för klient organisations nivå</span><span class="sxs-lookup"><span data-stu-id="333a9-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="333a9-113">Det här kommandot tar bort policyn för klient organisations nivå från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="333a9-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="333a9-114">Exempel 2: ta bort produktens policy princip</span><span class="sxs-lookup"><span data-stu-id="333a9-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="333a9-115">Det här kommandot tar bort produktens princip från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="333a9-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="333a9-116">Exempel 3: ta bort API-scope-principen</span><span class="sxs-lookup"><span data-stu-id="333a9-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="333a9-117">Det här kommandot tar bort API-scope-principen från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="333a9-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="333a9-118">Exempel 4: ta bort åtgärdens scope-princip</span><span class="sxs-lookup"><span data-stu-id="333a9-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="333a9-119">Det här kommandot tar bort åtgärdens omfattning från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="333a9-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="333a9-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="333a9-120">PARAMETERS</span></span>

### <span data-ttu-id="333a9-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="333a9-121">-ApiId</span></span>
<span data-ttu-id="333a9-122">Anger ID för ett befintligt API.</span><span class="sxs-lookup"><span data-stu-id="333a9-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="333a9-123">Om du anger den här parametern tar cmdleten bort API-scope-principen.</span><span class="sxs-lookup"><span data-stu-id="333a9-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="333a9-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="333a9-124">-Context</span></span>
<span data-ttu-id="333a9-125">Anger instansen för **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="333a9-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="333a9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333a9-126">-DefaultProfile</span></span>
<span data-ttu-id="333a9-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="333a9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="333a9-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="333a9-128">-OperationId</span></span>
<span data-ttu-id="333a9-129">Anger identifierare för en befintlig åtgärd.</span><span class="sxs-lookup"><span data-stu-id="333a9-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="333a9-130">Om du anger den här parametern med parametern *ApiId* tar denna cmdlet bort åtgärdens scope-princip.</span><span class="sxs-lookup"><span data-stu-id="333a9-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="333a9-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="333a9-131">-PassThru</span></span>
<span data-ttu-id="333a9-132">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="333a9-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="333a9-133">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="333a9-133">-ProductId</span></span>
<span data-ttu-id="333a9-134">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="333a9-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="333a9-135">Om du anger den här parametern tas produktens princip bort med cmdleten.</span><span class="sxs-lookup"><span data-stu-id="333a9-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="333a9-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="333a9-136">-Confirm</span></span>
<span data-ttu-id="333a9-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="333a9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="333a9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="333a9-138">-WhatIf</span></span>
<span data-ttu-id="333a9-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="333a9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="333a9-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="333a9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="333a9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333a9-141">CommonParameters</span></span>
<span data-ttu-id="333a9-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="333a9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333a9-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="333a9-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333a9-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="333a9-144">INPUTS</span></span>

### <span data-ttu-id="333a9-145">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="333a9-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="333a9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="333a9-146">System.String</span></span>

### <span data-ttu-id="333a9-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="333a9-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="333a9-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="333a9-148">OUTPUTS</span></span>

### <span data-ttu-id="333a9-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="333a9-149">System.Boolean</span></span>

## <span data-ttu-id="333a9-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="333a9-150">NOTES</span></span>

## <span data-ttu-id="333a9-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="333a9-151">RELATED LINKS</span></span>

[<span data-ttu-id="333a9-152">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="333a9-152">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="333a9-153">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="333a9-153">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


