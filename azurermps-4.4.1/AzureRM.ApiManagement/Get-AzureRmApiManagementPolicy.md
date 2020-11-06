---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 16eed643397245fa54b2876430042335762ea048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578684"
---
# <span data-ttu-id="4c19f-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4c19f-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="4c19f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c19f-102">SYNOPSIS</span></span>
<span data-ttu-id="4c19f-103">Hämtar den angivna omfattnings principen.</span><span class="sxs-lookup"><span data-stu-id="4c19f-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c19f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c19f-104">SYNTAX</span></span>

### <span data-ttu-id="4c19f-105">Klient organisations nivå (standard)</span><span class="sxs-lookup"><span data-stu-id="4c19f-105">Tenant level (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c19f-106">Produkt nivå</span><span class="sxs-lookup"><span data-stu-id="4c19f-106">Product level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c19f-107">API-nivå</span><span class="sxs-lookup"><span data-stu-id="4c19f-107">API level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c19f-108">Drifts nivå</span><span class="sxs-lookup"><span data-stu-id="4c19f-108">Operation level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c19f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c19f-109">DESCRIPTION</span></span>
<span data-ttu-id="4c19f-110">Cmdleten **Get-AzureRmApiManagementPolicy** hämtar den angivna omfattnings principen.</span><span class="sxs-lookup"><span data-stu-id="4c19f-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="4c19f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c19f-111">EXAMPLES</span></span>

### <span data-ttu-id="4c19f-112">Exempel 1: Hämta policy för klient organisations nivå</span><span class="sxs-lookup"><span data-stu-id="4c19f-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="4c19f-113">Det här kommandot får policyn för klient organisations nivå och sparar den i en fil med namnet tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="4c19f-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="4c19f-114">Exempel 2: skaffa produkt-scope policy</span><span class="sxs-lookup"><span data-stu-id="4c19f-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="4c19f-115">Det här kommandot får produkt omfattnings princip</span><span class="sxs-lookup"><span data-stu-id="4c19f-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="4c19f-116">Exempel 3: Hämta API-scope-policyn</span><span class="sxs-lookup"><span data-stu-id="4c19f-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

<span data-ttu-id="4c19f-117">Det här kommandot får API-scope-principer.</span><span class="sxs-lookup"><span data-stu-id="4c19f-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="4c19f-118">Exempel 4: Hämta operationens scope-princip</span><span class="sxs-lookup"><span data-stu-id="4c19f-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="4c19f-119">Det här kommandot hämtar åtgärdens scope-princip.</span><span class="sxs-lookup"><span data-stu-id="4c19f-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="4c19f-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c19f-120">PARAMETERS</span></span>

### <span data-ttu-id="4c19f-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4c19f-121">-ApiId</span></span>
<span data-ttu-id="4c19f-122">Anger ID för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="4c19f-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="4c19f-123">Om du anger den här parametern returnerar cmdleten API-scope-princip.</span><span class="sxs-lookup"><span data-stu-id="4c19f-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

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

### <span data-ttu-id="4c19f-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4c19f-124">-Context</span></span>
<span data-ttu-id="4c19f-125">Anger en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="4c19f-125">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="4c19f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="4c19f-126">-Force</span></span>
<span data-ttu-id="4c19f-127">ps_force</span><span class="sxs-lookup"><span data-stu-id="4c19f-127">ps_force</span></span>

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

### <span data-ttu-id="4c19f-128">-Format</span><span class="sxs-lookup"><span data-stu-id="4c19f-128">-Format</span></span>
<span data-ttu-id="4c19f-129">Anger formatet för API-hanterings principen.</span><span class="sxs-lookup"><span data-stu-id="4c19f-129">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="4c19f-130">Standardvärdet för den här parametern är "Application/VND. MS-Azure-APIM. policy + XML".</span><span class="sxs-lookup"><span data-stu-id="4c19f-130">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c19f-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="4c19f-131">-OperationId</span></span>
<span data-ttu-id="4c19f-132">Anger ID för den befintliga API-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="4c19f-132">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="4c19f-133">Om du anger den här parametern med *ApiId* cmdleten returnerar operation-scope-principen.</span><span class="sxs-lookup"><span data-stu-id="4c19f-133">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

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

### <span data-ttu-id="4c19f-134">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="4c19f-134">-ProductId</span></span>
<span data-ttu-id="4c19f-135">Anger identifieraren för en befintlig produkt.</span><span class="sxs-lookup"><span data-stu-id="4c19f-135">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="4c19f-136">Om du anger den här parametern returnerar cmdleten produktens omfattnings princip.</span><span class="sxs-lookup"><span data-stu-id="4c19f-136">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

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

### <span data-ttu-id="4c19f-137">-Spara som</span><span class="sxs-lookup"><span data-stu-id="4c19f-137">-SaveAs</span></span>
<span data-ttu-id="4c19f-138">Anger sökvägen som resultatet ska sparas till.</span><span class="sxs-lookup"><span data-stu-id="4c19f-138">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="4c19f-139">Om du inte anger den här parametern visas resultatet som en STING.</span><span class="sxs-lookup"><span data-stu-id="4c19f-139">If you do not specify this parameter the result is pipelined as a sting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c19f-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4c19f-140">-Confirm</span></span>
<span data-ttu-id="4c19f-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4c19f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c19f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c19f-142">-WhatIf</span></span>
<span data-ttu-id="4c19f-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4c19f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c19f-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4c19f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c19f-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c19f-145">-DefaultProfile</span></span>
<span data-ttu-id="4c19f-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c19f-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c19f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c19f-147">CommonParameters</span></span>
<span data-ttu-id="4c19f-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c19f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c19f-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c19f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c19f-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c19f-150">INPUTS</span></span>

## <span data-ttu-id="4c19f-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c19f-151">OUTPUTS</span></span>

### <span data-ttu-id="4c19f-152">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="4c19f-152">String</span></span>

## <span data-ttu-id="4c19f-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c19f-153">NOTES</span></span>

## <span data-ttu-id="4c19f-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c19f-154">RELATED LINKS</span></span>

[<span data-ttu-id="4c19f-155">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4c19f-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="4c19f-156">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4c19f-156">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


