---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 5f7fa78cb368afe3e277661122682f43f885f7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573767"
---
# <span data-ttu-id="bb741-101">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bb741-101">Remove-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="bb741-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb741-102">SYNOPSIS</span></span>
<span data-ttu-id="bb741-103">Tar bort API-hanteringskonsolen från ett angivet scope.</span><span class="sxs-lookup"><span data-stu-id="bb741-103">Removes the API Management policy from a specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb741-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb741-104">SYNTAX</span></span>

### <span data-ttu-id="bb741-105">Klient organisations nivå (standard)</span><span class="sxs-lookup"><span data-stu-id="bb741-105">Tenant level (Default)</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb741-106">Produkt nivå</span><span class="sxs-lookup"><span data-stu-id="bb741-106">Product level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb741-107">API-nivå</span><span class="sxs-lookup"><span data-stu-id="bb741-107">API level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb741-108">Drifts nivå</span><span class="sxs-lookup"><span data-stu-id="bb741-108">Operation level</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb741-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb741-109">DESCRIPTION</span></span>
<span data-ttu-id="bb741-110">Cmdleten **Remove-AzureRmApiManagementPolicy** tar bort API-hanterings principen från angivet scope.</span><span class="sxs-lookup"><span data-stu-id="bb741-110">The **Remove-AzureRmApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="bb741-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb741-111">EXAMPLES</span></span>

### <span data-ttu-id="bb741-112">Exempel 1: ta bort principen för klient organisations nivå</span><span class="sxs-lookup"><span data-stu-id="bb741-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext
```

<span data-ttu-id="bb741-113">Det här kommandot tar bort policyn för klient organisations nivå från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="bb741-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="bb741-114">Exempel 2: ta bort produktens policy princip</span><span class="sxs-lookup"><span data-stu-id="bb741-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="bb741-115">Det här kommandot tar bort produktens princip från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="bb741-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="bb741-116">Exempel 3: ta bort API-scope-principen</span><span class="sxs-lookup"><span data-stu-id="bb741-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

<span data-ttu-id="bb741-117">Det här kommandot tar bort API-scope-principen från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="bb741-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="bb741-118">Exempel 4: ta bort åtgärdens scope-princip</span><span class="sxs-lookup"><span data-stu-id="bb741-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>Remove-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="bb741-119">Det här kommandot tar bort åtgärdens omfattning från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="bb741-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="bb741-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb741-120">PARAMETERS</span></span>

### <span data-ttu-id="bb741-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bb741-121">-ApiId</span></span>
<span data-ttu-id="bb741-122">Anger ID för ett befintligt API.</span><span class="sxs-lookup"><span data-stu-id="bb741-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="bb741-123">Om du anger den här parametern tar cmdleten bort API-scope-principen.</span><span class="sxs-lookup"><span data-stu-id="bb741-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb741-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="bb741-124">-Context</span></span>
<span data-ttu-id="bb741-125">Anger instansen för **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="bb741-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bb741-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="bb741-126">-OperationId</span></span>
<span data-ttu-id="bb741-127">Anger identifierare för en befintlig åtgärd.</span><span class="sxs-lookup"><span data-stu-id="bb741-127">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="bb741-128">Om du anger den här parametern med parametern *ApiId* tar denna cmdlet bort åtgärdens scope-princip.</span><span class="sxs-lookup"><span data-stu-id="bb741-128">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb741-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb741-129">-PassThru</span></span>
<span data-ttu-id="bb741-130">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="bb741-130">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="bb741-131">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="bb741-131">-ProductId</span></span>
<span data-ttu-id="bb741-132">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="bb741-132">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="bb741-133">Om du anger den här parametern tas produktens princip bort med cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb741-133">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb741-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bb741-134">-Confirm</span></span>
<span data-ttu-id="bb741-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb741-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb741-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb741-136">-WhatIf</span></span>
<span data-ttu-id="bb741-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bb741-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb741-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bb741-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb741-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb741-139">-DefaultProfile</span></span>
<span data-ttu-id="bb741-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bb741-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb741-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb741-141">CommonParameters</span></span>
<span data-ttu-id="bb741-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb741-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb741-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb741-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb741-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb741-144">INPUTS</span></span>

## <span data-ttu-id="bb741-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb741-145">OUTPUTS</span></span>

### <span data-ttu-id="bb741-146">Returtyp</span><span class="sxs-lookup"><span data-stu-id="bb741-146">Boolean</span></span>

## <span data-ttu-id="bb741-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb741-147">NOTES</span></span>

## <span data-ttu-id="bb741-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb741-148">RELATED LINKS</span></span>

[<span data-ttu-id="bb741-149">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bb741-149">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="bb741-150">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bb741-150">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


