---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 8073df3946f5bf42ee8b0e5f2c7ae7881e905eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578599"
---
# <span data-ttu-id="8b05e-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8b05e-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="8b05e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b05e-102">SYNOPSIS</span></span>
<span data-ttu-id="8b05e-103">Ställer in den angivna scopealternativ för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="8b05e-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b05e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b05e-104">SYNTAX</span></span>

### <span data-ttu-id="8b05e-105">Klient organisations nivå (standard)</span><span class="sxs-lookup"><span data-stu-id="8b05e-105">Tenant level (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b05e-106">Produkt nivå</span><span class="sxs-lookup"><span data-stu-id="8b05e-106">Product level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b05e-107">API-nivå</span><span class="sxs-lookup"><span data-stu-id="8b05e-107">API level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b05e-108">Drifts nivå</span><span class="sxs-lookup"><span data-stu-id="8b05e-108">Operation level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b05e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b05e-109">DESCRIPTION</span></span>
<span data-ttu-id="8b05e-110">Cmdleten **set-AzureRmApiManagementPolicy** anger den angivna SCOPEALTERNATIV för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="8b05e-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="8b05e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b05e-111">EXAMPLES</span></span>

### <span data-ttu-id="8b05e-112">Exempel 1: ange principen för klient organisations nivå</span><span class="sxs-lookup"><span data-stu-id="8b05e-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="8b05e-113">Det här kommandot anger principer för klient organisations nivå från en fil med namnet tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="8b05e-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="8b05e-114">Exempel 2: Ange en produkt omfattnings princip</span><span class="sxs-lookup"><span data-stu-id="8b05e-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="8b05e-115">Det här kommandot ställer in produkt omfattnings princip för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="8b05e-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="8b05e-116">Exempel 3: Ange API-scope-princip</span><span class="sxs-lookup"><span data-stu-id="8b05e-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="8b05e-117">Det här kommandot anger API-scopealternativ för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="8b05e-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="8b05e-118">Exempel 4: Ange åtgärds områdes princip</span><span class="sxs-lookup"><span data-stu-id="8b05e-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="8b05e-119">Det här kommandot anger åtgärds omfattnings princip för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="8b05e-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="8b05e-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b05e-120">PARAMETERS</span></span>

### <span data-ttu-id="8b05e-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8b05e-121">-ApiId</span></span>
<span data-ttu-id="8b05e-122">Anger ID för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="8b05e-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="8b05e-123">Om du anger den här parametern ställer cmdleten in API-scope-principen.</span><span class="sxs-lookup"><span data-stu-id="8b05e-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="8b05e-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="8b05e-124">-Context</span></span>
<span data-ttu-id="8b05e-125">Anger instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="8b05e-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="8b05e-126">-Format</span><span class="sxs-lookup"><span data-stu-id="8b05e-126">-Format</span></span>
<span data-ttu-id="8b05e-127">Anger principens format.</span><span class="sxs-lookup"><span data-stu-id="8b05e-127">Specifies the format of the policy.</span></span>
<span data-ttu-id="8b05e-128">Standardvärdet är "Application/VND. MS-Azure-APIM. policy + XML".</span><span class="sxs-lookup"><span data-stu-id="8b05e-128">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="8b05e-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="8b05e-129">-OperationId</span></span>
<span data-ttu-id="8b05e-130">Anger identifierare för den befintliga åtgärden.</span><span class="sxs-lookup"><span data-stu-id="8b05e-130">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="8b05e-131">Om det anges med ApiId kommer att ange åtgärds omfattnings princip.</span><span class="sxs-lookup"><span data-stu-id="8b05e-131">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="8b05e-132">De här parametrarna är obligatoriska.</span><span class="sxs-lookup"><span data-stu-id="8b05e-132">This parameters is required.</span></span>

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

### <span data-ttu-id="8b05e-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b05e-133">-PassThru</span></span>
<span data-ttu-id="8b05e-134">passthru</span><span class="sxs-lookup"><span data-stu-id="8b05e-134">passthru</span></span>

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

### <span data-ttu-id="8b05e-135">-Princip</span><span class="sxs-lookup"><span data-stu-id="8b05e-135">-Policy</span></span>
<span data-ttu-id="8b05e-136">Anger princip dokumentet som en sträng.</span><span class="sxs-lookup"><span data-stu-id="8b05e-136">Specifies the policy document as a string.</span></span>
<span data-ttu-id="8b05e-137">Denna parameter är obligatorisk om parametern- *PolicyFilePath* inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="8b05e-137">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="8b05e-138">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="8b05e-138">-PolicyFilePath</span></span>
<span data-ttu-id="8b05e-139">Anger sökvägen till princip dokumentet.</span><span class="sxs-lookup"><span data-stu-id="8b05e-139">Specifies the policy document file path.</span></span>
<span data-ttu-id="8b05e-140">Den här parametern är obligatorisk om parametern *policy* inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="8b05e-140">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="8b05e-141">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="8b05e-141">-ProductId</span></span>
<span data-ttu-id="8b05e-142">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="8b05e-142">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="8b05e-143">Om denna parameter anges ställer cmdleten in produktens princip policy.</span><span class="sxs-lookup"><span data-stu-id="8b05e-143">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="8b05e-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b05e-144">-DefaultProfile</span></span>
<span data-ttu-id="8b05e-145">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b05e-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b05e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b05e-146">CommonParameters</span></span>
<span data-ttu-id="8b05e-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b05e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b05e-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b05e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b05e-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b05e-149">INPUTS</span></span>

## <span data-ttu-id="8b05e-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b05e-150">OUTPUTS</span></span>

### <span data-ttu-id="8b05e-151">bool</span><span class="sxs-lookup"><span data-stu-id="8b05e-151">bool</span></span>

## <span data-ttu-id="8b05e-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b05e-152">NOTES</span></span>

## <span data-ttu-id="8b05e-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b05e-153">RELATED LINKS</span></span>

[<span data-ttu-id="8b05e-154">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8b05e-154">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="8b05e-155">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8b05e-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


