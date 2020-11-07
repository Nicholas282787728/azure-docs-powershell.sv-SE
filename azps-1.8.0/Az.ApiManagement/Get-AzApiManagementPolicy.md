---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: 0da4e2168ccc7f5a62aa4265af3b7823dd4cb050
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743404"
---
# <span data-ttu-id="75273-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="75273-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="75273-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75273-102">SYNOPSIS</span></span>
<span data-ttu-id="75273-103">Hämtar den angivna omfattnings principen.</span><span class="sxs-lookup"><span data-stu-id="75273-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="75273-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75273-104">SYNTAX</span></span>

### <span data-ttu-id="75273-105">GetTenantLevel (standard)</span><span class="sxs-lookup"><span data-stu-id="75273-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75273-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="75273-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75273-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="75273-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75273-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="75273-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75273-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75273-109">DESCRIPTION</span></span>
<span data-ttu-id="75273-110">Cmdleten **Get-AzApiManagementPolicy** hämtar den angivna omfattnings principen.</span><span class="sxs-lookup"><span data-stu-id="75273-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="75273-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75273-111">EXAMPLES</span></span>

### <span data-ttu-id="75273-112">Exempel 1: Hämta policy för klient organisations nivå</span><span class="sxs-lookup"><span data-stu-id="75273-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="75273-113">Det här kommandot får policyn för klient organisations nivå och sparar den i en fil med namnet tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="75273-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="75273-114">Exempel 2: skaffa produkt-scope policy</span><span class="sxs-lookup"><span data-stu-id="75273-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="75273-115">Det här kommandot får produkt omfattnings princip</span><span class="sxs-lookup"><span data-stu-id="75273-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="75273-116">Exempel 3: Hämta API-scope-policyn</span><span class="sxs-lookup"><span data-stu-id="75273-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="75273-117">Det här kommandot får API-scope-principer.</span><span class="sxs-lookup"><span data-stu-id="75273-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="75273-118">Exempel 4: Hämta operationens scope-princip</span><span class="sxs-lookup"><span data-stu-id="75273-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="75273-119">Det här kommandot hämtar åtgärdens scope-princip.</span><span class="sxs-lookup"><span data-stu-id="75273-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="75273-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75273-120">PARAMETERS</span></span>

### <span data-ttu-id="75273-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="75273-121">-ApiId</span></span>
<span data-ttu-id="75273-122">Anger ID för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="75273-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="75273-123">Om du anger den här parametern returnerar cmdleten API-scope-princip.</span><span class="sxs-lookup"><span data-stu-id="75273-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75273-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="75273-124">-ApiRevision</span></span>
<span data-ttu-id="75273-125">Identifierare för API-revision.</span><span class="sxs-lookup"><span data-stu-id="75273-125">Identifier of API Revision.</span></span> <span data-ttu-id="75273-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="75273-126">This parameter is optional.</span></span> <span data-ttu-id="75273-127">Om det inte anges hämtas policyn från den för tillfället aktiva API-ändringen.</span><span class="sxs-lookup"><span data-stu-id="75273-127">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75273-128">-Kontext</span><span class="sxs-lookup"><span data-stu-id="75273-128">-Context</span></span>
<span data-ttu-id="75273-129">Anger en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="75273-129">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="75273-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75273-130">-DefaultProfile</span></span>
<span data-ttu-id="75273-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75273-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75273-132">-Force</span><span class="sxs-lookup"><span data-stu-id="75273-132">-Force</span></span>
<span data-ttu-id="75273-133">ps_force</span><span class="sxs-lookup"><span data-stu-id="75273-133">ps_force</span></span>

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

### <span data-ttu-id="75273-134">-Format</span><span class="sxs-lookup"><span data-stu-id="75273-134">-Format</span></span>
<span data-ttu-id="75273-135">Anger formatet för API-hanterings principen.</span><span class="sxs-lookup"><span data-stu-id="75273-135">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="75273-136">Standardvärdet för den här parametern är "Application/VND. MS-AZ-APIM. policy + XML".</span><span class="sxs-lookup"><span data-stu-id="75273-136">The default value for this parameter is "application/vnd.ms-az-apim.policy+xml".</span></span>

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

### <span data-ttu-id="75273-137">-OperationId</span><span class="sxs-lookup"><span data-stu-id="75273-137">-OperationId</span></span>
<span data-ttu-id="75273-138">Anger ID för den befintliga API-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="75273-138">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="75273-139">Om du anger den här parametern med *ApiId* cmdleten returnerar operation-scope-principen.</span><span class="sxs-lookup"><span data-stu-id="75273-139">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75273-140">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="75273-140">-ProductId</span></span>
<span data-ttu-id="75273-141">Anger identifieraren för en befintlig produkt.</span><span class="sxs-lookup"><span data-stu-id="75273-141">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="75273-142">Om du anger den här parametern returnerar cmdleten produktens omfattnings princip.</span><span class="sxs-lookup"><span data-stu-id="75273-142">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75273-143">-Spara som</span><span class="sxs-lookup"><span data-stu-id="75273-143">-SaveAs</span></span>
<span data-ttu-id="75273-144">Anger sökvägen som resultatet ska sparas till.</span><span class="sxs-lookup"><span data-stu-id="75273-144">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="75273-145">Om du inte anger den här parametern visas resultatet som en STING.</span><span class="sxs-lookup"><span data-stu-id="75273-145">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="75273-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75273-146">-Confirm</span></span>
<span data-ttu-id="75273-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75273-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75273-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75273-148">-WhatIf</span></span>
<span data-ttu-id="75273-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75273-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75273-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75273-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75273-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75273-151">CommonParameters</span></span>
<span data-ttu-id="75273-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75273-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75273-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75273-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75273-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75273-154">INPUTS</span></span>

### <span data-ttu-id="75273-155">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="75273-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="75273-156">System. String</span><span class="sxs-lookup"><span data-stu-id="75273-156">System.String</span></span>

### <span data-ttu-id="75273-157">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="75273-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="75273-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75273-158">OUTPUTS</span></span>

### <span data-ttu-id="75273-159">System. String</span><span class="sxs-lookup"><span data-stu-id="75273-159">System.String</span></span>

## <span data-ttu-id="75273-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75273-160">NOTES</span></span>

## <span data-ttu-id="75273-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75273-161">RELATED LINKS</span></span>

[<span data-ttu-id="75273-162">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="75273-162">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="75273-163">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="75273-163">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


