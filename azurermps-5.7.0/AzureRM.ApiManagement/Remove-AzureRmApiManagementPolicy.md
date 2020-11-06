---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 67cff03f8531ff71170fe565d5da411ca5b4f127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573579"
---
# <span data-ttu-id="06592-101">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="06592-101">Remove-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="06592-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06592-102">SYNOPSIS</span></span>
<span data-ttu-id="06592-103">Tar bort API-hanteringskonsolen från ett angivet scope.</span><span class="sxs-lookup"><span data-stu-id="06592-103">Removes the API Management policy from a specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06592-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06592-104">SYNTAX</span></span>

### <span data-ttu-id="06592-105">RemoveTenantLevel (standard)</span><span class="sxs-lookup"><span data-stu-id="06592-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06592-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="06592-106">RemoveProductLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06592-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="06592-107">RemoveApiLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06592-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="06592-108">RemoveOperationLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06592-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06592-109">DESCRIPTION</span></span>
<span data-ttu-id="06592-110">Cmdleten **Remove-AzureRmApiManagementPolicy** tar bort API-hanterings principen från angivet scope.</span><span class="sxs-lookup"><span data-stu-id="06592-110">The **Remove-AzureRmApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="06592-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06592-111">EXAMPLES</span></span>

### <span data-ttu-id="06592-112">Exempel 1: ta bort principen för klient organisations nivå</span><span class="sxs-lookup"><span data-stu-id="06592-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="06592-113">Det här kommandot tar bort policyn för klient organisations nivå från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="06592-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="06592-114">Exempel 2: ta bort produktens policy princip</span><span class="sxs-lookup"><span data-stu-id="06592-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="06592-115">Det här kommandot tar bort produktens princip från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="06592-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="06592-116">Exempel 3: ta bort API-scope-principen</span><span class="sxs-lookup"><span data-stu-id="06592-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="06592-117">Det här kommandot tar bort API-scope-principen från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="06592-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="06592-118">Exempel 4: ta bort åtgärdens scope-princip</span><span class="sxs-lookup"><span data-stu-id="06592-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="06592-119">Det här kommandot tar bort åtgärdens omfattning från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="06592-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="06592-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06592-120">PARAMETERS</span></span>

### <span data-ttu-id="06592-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="06592-121">-ApiId</span></span>
<span data-ttu-id="06592-122">Anger ID för ett befintligt API.</span><span class="sxs-lookup"><span data-stu-id="06592-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="06592-123">Om du anger den här parametern tar cmdleten bort API-scope-principen.</span><span class="sxs-lookup"><span data-stu-id="06592-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: RemoveApiLevel, RemoveOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06592-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="06592-124">-Context</span></span>
<span data-ttu-id="06592-125">Anger instansen för **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="06592-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06592-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06592-126">-DefaultProfile</span></span>
<span data-ttu-id="06592-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06592-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06592-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="06592-128">-OperationId</span></span>
<span data-ttu-id="06592-129">Anger identifierare för en befintlig åtgärd.</span><span class="sxs-lookup"><span data-stu-id="06592-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="06592-130">Om du anger den här parametern med parametern *ApiId* tar denna cmdlet bort åtgärdens scope-princip.</span><span class="sxs-lookup"><span data-stu-id="06592-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: RemoveOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06592-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06592-131">-PassThru</span></span>
<span data-ttu-id="06592-132">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="06592-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06592-133">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="06592-133">-ProductId</span></span>
<span data-ttu-id="06592-134">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="06592-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="06592-135">Om du anger den här parametern tas produktens princip bort med cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06592-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: RemoveProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06592-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06592-136">-Confirm</span></span>
<span data-ttu-id="06592-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06592-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06592-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06592-138">-WhatIf</span></span>
<span data-ttu-id="06592-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06592-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06592-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06592-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06592-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06592-141">CommonParameters</span></span>
<span data-ttu-id="06592-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06592-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06592-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06592-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06592-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06592-144">INPUTS</span></span>

### <span data-ttu-id="06592-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="06592-145">None</span></span>
<span data-ttu-id="06592-146">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="06592-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06592-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06592-147">OUTPUTS</span></span>

### <span data-ttu-id="06592-148">Returtyp</span><span class="sxs-lookup"><span data-stu-id="06592-148">Boolean</span></span>

## <span data-ttu-id="06592-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06592-149">NOTES</span></span>

## <span data-ttu-id="06592-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06592-150">RELATED LINKS</span></span>

[<span data-ttu-id="06592-151">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="06592-151">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="06592-152">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="06592-152">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


