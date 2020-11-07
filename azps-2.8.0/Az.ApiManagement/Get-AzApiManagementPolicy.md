---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: fa065aa7e56572fbcb58fd78a3feff4a0909be9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745826"
---
# <span data-ttu-id="511c8-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="511c8-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="511c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="511c8-102">SYNOPSIS</span></span>
<span data-ttu-id="511c8-103">Hämtar den angivna omfattnings principen.</span><span class="sxs-lookup"><span data-stu-id="511c8-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="511c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="511c8-104">SYNTAX</span></span>

### <span data-ttu-id="511c8-105">GetTenantLevel (standard)</span><span class="sxs-lookup"><span data-stu-id="511c8-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="511c8-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="511c8-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="511c8-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="511c8-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="511c8-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="511c8-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="511c8-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="511c8-109">DESCRIPTION</span></span>
<span data-ttu-id="511c8-110">Cmdleten **Get-AzApiManagementPolicy** hämtar den angivna omfattnings principen.</span><span class="sxs-lookup"><span data-stu-id="511c8-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="511c8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="511c8-111">EXAMPLES</span></span>

### <span data-ttu-id="511c8-112">Exempel 1: Hämta policy för klient organisations nivå</span><span class="sxs-lookup"><span data-stu-id="511c8-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="511c8-113">Det här kommandot får policyn för klient organisations nivå och sparar den i en fil med namnet tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="511c8-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="511c8-114">Exempel 2: skaffa produkt-scope policy</span><span class="sxs-lookup"><span data-stu-id="511c8-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="511c8-115">Det här kommandot får produkt omfattnings princip</span><span class="sxs-lookup"><span data-stu-id="511c8-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="511c8-116">Exempel 3: Hämta API-scope-policyn</span><span class="sxs-lookup"><span data-stu-id="511c8-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="511c8-117">Det här kommandot får API-scope-principer.</span><span class="sxs-lookup"><span data-stu-id="511c8-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="511c8-118">Exempel 4: Hämta operationens scope-princip</span><span class="sxs-lookup"><span data-stu-id="511c8-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="511c8-119">Det här kommandot hämtar åtgärdens scope-princip.</span><span class="sxs-lookup"><span data-stu-id="511c8-119">This command gets the operation-scope policy.</span></span>

### <span data-ttu-id="511c8-120">Exempel 5: Hämta principer för klient organisations omfattning i RawXml-format</span><span class="sxs-lookup"><span data-stu-id="511c8-120">Example 5: Get the Tenant scope policy in RawXml format</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS c:\> Get-AzApiManagementPolicy -Context $context -Format rawxml

<policies>
        <inbound>
                <set-header name="correlationid" exists-action="skip">
                        <value>@{
                var guidBinary = new byte[16];
                Array.Copy(Guid.NewGuid().ToByteArray(), 0, guidBinary, 0, 10);
                long time = DateTime.Now.Ticks;
                byte[] bytes = new byte[6];
                unchecked
                {
                       bytes[5] = (byte)(time >> 40);
                       bytes[4] = (byte)(time >> 32);
                       bytes[3] = (byte)(time >> 24);
                       bytes[2] = (byte)(time >> 16);
                       bytes[1] = (byte)(time >> 8);
                       bytes[0] = (byte)(time);
                }
                Array.Copy(bytes, 0, guidBinary, 10, 6);
                return new Guid(guidBinary).ToString();
            }
            </value>
                </set-header>
        </inbound>
        <backend>
                <forward-request />
        </backend>
        <outbound />
        <on-error />
</policies>
```

<span data-ttu-id="511c8-121">Det här kommandot hämtar principer för klient organisations omfattning i icke-XML-avbrotts format.</span><span class="sxs-lookup"><span data-stu-id="511c8-121">This command gets the tenant-scope policy in Non-Xml escaped format.</span></span>

## <span data-ttu-id="511c8-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="511c8-122">PARAMETERS</span></span>

### <span data-ttu-id="511c8-123">-ApiId</span><span class="sxs-lookup"><span data-stu-id="511c8-123">-ApiId</span></span>
<span data-ttu-id="511c8-124">Anger ID för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="511c8-124">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="511c8-125">Om du anger den här parametern returnerar cmdleten API-scope-princip.</span><span class="sxs-lookup"><span data-stu-id="511c8-125">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

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

### <span data-ttu-id="511c8-126">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="511c8-126">-ApiRevision</span></span>
<span data-ttu-id="511c8-127">Identifierare för API-revision.</span><span class="sxs-lookup"><span data-stu-id="511c8-127">Identifier of API Revision.</span></span> <span data-ttu-id="511c8-128">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="511c8-128">This parameter is optional.</span></span> <span data-ttu-id="511c8-129">Om det inte anges hämtas policyn från den för tillfället aktiva API-ändringen.</span><span class="sxs-lookup"><span data-stu-id="511c8-129">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="511c8-130">-Kontext</span><span class="sxs-lookup"><span data-stu-id="511c8-130">-Context</span></span>
<span data-ttu-id="511c8-131">Anger en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="511c8-131">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="511c8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="511c8-132">-DefaultProfile</span></span>
<span data-ttu-id="511c8-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="511c8-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="511c8-134">-Force</span><span class="sxs-lookup"><span data-stu-id="511c8-134">-Force</span></span>
<span data-ttu-id="511c8-135">ps_force</span><span class="sxs-lookup"><span data-stu-id="511c8-135">ps_force</span></span>

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

### <span data-ttu-id="511c8-136">-Format</span><span class="sxs-lookup"><span data-stu-id="511c8-136">-Format</span></span>
<span data-ttu-id="511c8-137">Anger formatet för API-hanterings principen.</span><span class="sxs-lookup"><span data-stu-id="511c8-137">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="511c8-138">Standardvärdet för den här parametern är "XML".</span><span class="sxs-lookup"><span data-stu-id="511c8-138">The default value for this parameter is "xml".</span></span>

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

### <span data-ttu-id="511c8-139">-OperationId</span><span class="sxs-lookup"><span data-stu-id="511c8-139">-OperationId</span></span>
<span data-ttu-id="511c8-140">Anger ID för den befintliga API-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="511c8-140">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="511c8-141">Om du anger den här parametern med *ApiId* cmdleten returnerar operation-scope-principen.</span><span class="sxs-lookup"><span data-stu-id="511c8-141">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

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

### <span data-ttu-id="511c8-142">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="511c8-142">-ProductId</span></span>
<span data-ttu-id="511c8-143">Anger identifieraren för en befintlig produkt.</span><span class="sxs-lookup"><span data-stu-id="511c8-143">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="511c8-144">Om du anger den här parametern returnerar cmdleten produktens omfattnings princip.</span><span class="sxs-lookup"><span data-stu-id="511c8-144">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

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

### <span data-ttu-id="511c8-145">-Spara som</span><span class="sxs-lookup"><span data-stu-id="511c8-145">-SaveAs</span></span>
<span data-ttu-id="511c8-146">Anger sökvägen som resultatet ska sparas till.</span><span class="sxs-lookup"><span data-stu-id="511c8-146">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="511c8-147">Om du inte anger den här parametern visas resultatet som en STING.</span><span class="sxs-lookup"><span data-stu-id="511c8-147">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="511c8-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="511c8-148">-Confirm</span></span>
<span data-ttu-id="511c8-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="511c8-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="511c8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="511c8-150">-WhatIf</span></span>
<span data-ttu-id="511c8-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="511c8-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="511c8-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="511c8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="511c8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511c8-153">CommonParameters</span></span>
<span data-ttu-id="511c8-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="511c8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511c8-155">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="511c8-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511c8-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="511c8-156">INPUTS</span></span>

### <span data-ttu-id="511c8-157">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="511c8-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="511c8-158">System. String</span><span class="sxs-lookup"><span data-stu-id="511c8-158">System.String</span></span>

### <span data-ttu-id="511c8-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="511c8-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="511c8-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="511c8-160">OUTPUTS</span></span>

### <span data-ttu-id="511c8-161">System. String</span><span class="sxs-lookup"><span data-stu-id="511c8-161">System.String</span></span>

## <span data-ttu-id="511c8-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="511c8-162">NOTES</span></span>

## <span data-ttu-id="511c8-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="511c8-163">RELATED LINKS</span></span>

[<span data-ttu-id="511c8-164">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="511c8-164">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="511c8-165">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="511c8-165">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


