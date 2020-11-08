---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: ee0a95653dbc949518c485554c6202664d943ba3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272952"
---
# <span data-ttu-id="7656a-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7656a-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="7656a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7656a-102">SYNOPSIS</span></span>
<span data-ttu-id="7656a-103">Ställer in den angivna scopealternativ för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="7656a-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="7656a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7656a-104">SYNTAX</span></span>

### <span data-ttu-id="7656a-105">SetTenantLevel (standard)</span><span class="sxs-lookup"><span data-stu-id="7656a-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7656a-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="7656a-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7656a-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="7656a-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7656a-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="7656a-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7656a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7656a-109">DESCRIPTION</span></span>
<span data-ttu-id="7656a-110">Cmdleten **set-AzApiManagementPolicy** anger den angivna SCOPEALTERNATIV för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="7656a-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="7656a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7656a-111">EXAMPLES</span></span>

### <span data-ttu-id="7656a-112">Exempel 1: ange principen för klient organisations nivå</span><span class="sxs-lookup"><span data-stu-id="7656a-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="7656a-113">Det här kommandot anger principer för klient organisations nivå från en fil med namnet tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="7656a-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="7656a-114">Exempel 2: Ange en produkt omfattnings princip</span><span class="sxs-lookup"><span data-stu-id="7656a-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="7656a-115">Det här kommandot ställer in produkt omfattnings princip för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="7656a-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="7656a-116">Exempel 3: Ange API-scope-princip</span><span class="sxs-lookup"><span data-stu-id="7656a-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="7656a-117">Det här kommandot anger API-scopealternativ för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="7656a-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="7656a-118">Exempel 4: Ange åtgärds områdes princip</span><span class="sxs-lookup"><span data-stu-id="7656a-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="7656a-119">Det här kommandot anger åtgärds omfattnings princip för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="7656a-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="7656a-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7656a-120">PARAMETERS</span></span>

### <span data-ttu-id="7656a-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7656a-121">-ApiId</span></span>
<span data-ttu-id="7656a-122">Anger ID för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="7656a-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="7656a-123">Om du anger den här parametern ställer cmdleten in API-scope-principen.</span><span class="sxs-lookup"><span data-stu-id="7656a-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7656a-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="7656a-124">-ApiRevision</span></span>
<span data-ttu-id="7656a-125">Identifierare för API-revision.</span><span class="sxs-lookup"><span data-stu-id="7656a-125">Identifier of API Revision.</span></span> <span data-ttu-id="7656a-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="7656a-126">This parameter is optional.</span></span> <span data-ttu-id="7656a-127">Om det inte anges uppdateras policyn i den för tillfället aktiva API-ändringen.</span><span class="sxs-lookup"><span data-stu-id="7656a-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7656a-128">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7656a-128">-Context</span></span>
<span data-ttu-id="7656a-129">Anger instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="7656a-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="7656a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7656a-130">-DefaultProfile</span></span>
<span data-ttu-id="7656a-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7656a-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7656a-132">-Format</span><span class="sxs-lookup"><span data-stu-id="7656a-132">-Format</span></span>
<span data-ttu-id="7656a-133">Anger principens format.</span><span class="sxs-lookup"><span data-stu-id="7656a-133">Specifies the format of the policy.</span></span> <span data-ttu-id="7656a-134">Om `application/vnd.ms-azure-apim.policy+xml` du använder, måste uttryck i principen vara XML-avmarkerat.</span><span class="sxs-lookup"><span data-stu-id="7656a-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="7656a-135">När du använder `application/vnd.ms-azure-apim.policy.raw+xml` den är det **inte** nödvändigt att principen är avmarkerad.</span><span class="sxs-lookup"><span data-stu-id="7656a-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="7656a-136">Standardvärdet är `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="7656a-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="7656a-137">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="7656a-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="7656a-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7656a-138">-OperationId</span></span>
<span data-ttu-id="7656a-139">Anger identifierare för den befintliga åtgärden.</span><span class="sxs-lookup"><span data-stu-id="7656a-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="7656a-140">Om det anges med ApiId kommer att ange åtgärds omfattnings princip.</span><span class="sxs-lookup"><span data-stu-id="7656a-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="7656a-141">De här parametrarna är obligatoriska.</span><span class="sxs-lookup"><span data-stu-id="7656a-141">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7656a-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7656a-142">-PassThru</span></span>
<span data-ttu-id="7656a-143">passthru</span><span class="sxs-lookup"><span data-stu-id="7656a-143">passthru</span></span>

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

### <span data-ttu-id="7656a-144">-Princip</span><span class="sxs-lookup"><span data-stu-id="7656a-144">-Policy</span></span>
<span data-ttu-id="7656a-145">Anger princip dokumentet som en sträng.</span><span class="sxs-lookup"><span data-stu-id="7656a-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="7656a-146">Denna parameter är obligatorisk om parametern- *PolicyFilePath* inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="7656a-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="7656a-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="7656a-147">-PolicyFilePath</span></span>
<span data-ttu-id="7656a-148">Anger sökvägen till princip dokumentet.</span><span class="sxs-lookup"><span data-stu-id="7656a-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="7656a-149">Den här parametern är obligatorisk om parametern *policy* inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="7656a-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="7656a-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="7656a-150">-PolicyUrl</span></span>
<span data-ttu-id="7656a-151">URL-adressen där princip dokumentet finns.</span><span class="sxs-lookup"><span data-stu-id="7656a-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="7656a-152">Den här parametern är obligatorisk om-princip-eller-PolicyFilePath inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="7656a-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="7656a-153">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="7656a-153">-ProductId</span></span>
<span data-ttu-id="7656a-154">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="7656a-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="7656a-155">Om denna parameter anges ställer cmdleten in produktens princip policy.</span><span class="sxs-lookup"><span data-stu-id="7656a-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7656a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7656a-156">CommonParameters</span></span>
<span data-ttu-id="7656a-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7656a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7656a-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7656a-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7656a-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7656a-159">INPUTS</span></span>

### <span data-ttu-id="7656a-160">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7656a-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7656a-161">System. String</span><span class="sxs-lookup"><span data-stu-id="7656a-161">System.String</span></span>

### <span data-ttu-id="7656a-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7656a-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7656a-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7656a-163">OUTPUTS</span></span>

### <span data-ttu-id="7656a-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7656a-164">System.Boolean</span></span>

## <span data-ttu-id="7656a-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7656a-165">NOTES</span></span>

## <span data-ttu-id="7656a-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7656a-166">RELATED LINKS</span></span>

[<span data-ttu-id="7656a-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7656a-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="7656a-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7656a-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)


