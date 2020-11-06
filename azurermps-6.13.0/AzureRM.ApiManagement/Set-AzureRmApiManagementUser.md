---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: 705deeb8e9b248b480bd2a28662cc7e968f8c228
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574060"
---
# <span data-ttu-id="bde39-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bde39-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="bde39-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bde39-102">SYNOPSIS</span></span>
<span data-ttu-id="bde39-103">Anger användar information.</span><span class="sxs-lookup"><span data-stu-id="bde39-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bde39-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bde39-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bde39-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bde39-105">DESCRIPTION</span></span>
<span data-ttu-id="bde39-106">Cmdleten **set-AzureRmApiManagementUser** anger användar information.</span><span class="sxs-lookup"><span data-stu-id="bde39-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="bde39-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bde39-107">EXAMPLES</span></span>

### <span data-ttu-id="bde39-108">Exempel 1: ändra en användares lösen ord, e-postadress och status</span><span class="sxs-lookup"><span data-stu-id="bde39-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="bde39-109">Det här kommandot anger ett nytt lösen ord och en e-postadress för användaren.</span><span class="sxs-lookup"><span data-stu-id="bde39-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="bde39-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bde39-110">PARAMETERS</span></span>

### <span data-ttu-id="bde39-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="bde39-111">-Context</span></span>
<span data-ttu-id="bde39-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bde39-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="bde39-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="bde39-113">This parameter is required.</span></span>

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

### <span data-ttu-id="bde39-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bde39-114">-DefaultProfile</span></span>
<span data-ttu-id="bde39-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bde39-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bde39-116">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="bde39-116">-Email</span></span>
<span data-ttu-id="bde39-117">Anger användarens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="bde39-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="bde39-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="bde39-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="bde39-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="bde39-119">-FirstName</span></span>
<span data-ttu-id="bde39-120">Anger användarens förnamn.</span><span class="sxs-lookup"><span data-stu-id="bde39-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="bde39-121">Parametern måste vara 1 till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="bde39-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="bde39-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="bde39-122">-LastName</span></span>
<span data-ttu-id="bde39-123">Anger användarens efter namn.</span><span class="sxs-lookup"><span data-stu-id="bde39-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="bde39-124">Parametern måste vara 1 till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="bde39-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="bde39-125">-Obs!</span><span class="sxs-lookup"><span data-stu-id="bde39-125">-Note</span></span>
<span data-ttu-id="bde39-126">Anger en kommentar om användaren.</span><span class="sxs-lookup"><span data-stu-id="bde39-126">Specifies a note about the user.</span></span>
<span data-ttu-id="bde39-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="bde39-127">This parameter is optional.</span></span>
<span data-ttu-id="bde39-128">Standardvärdet för den här parametern är $null.</span><span class="sxs-lookup"><span data-stu-id="bde39-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="bde39-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bde39-129">-PassThru</span></span>
<span data-ttu-id="bde39-130">passthru</span><span class="sxs-lookup"><span data-stu-id="bde39-130">passthru</span></span>

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

### <span data-ttu-id="bde39-131">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="bde39-131">-Password</span></span>
<span data-ttu-id="bde39-132">Anger användarens lösen ord.</span><span class="sxs-lookup"><span data-stu-id="bde39-132">Specifies the user password.</span></span>
<span data-ttu-id="bde39-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="bde39-133">This parameter is optional.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde39-134">-State</span><span class="sxs-lookup"><span data-stu-id="bde39-134">-State</span></span>
<span data-ttu-id="bde39-135">Anger användar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="bde39-135">Specifies the user state.</span></span>
<span data-ttu-id="bde39-136">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="bde39-136">This parameter is optional.</span></span>
<span data-ttu-id="bde39-137">Standardvärdet är aktivt.</span><span class="sxs-lookup"><span data-stu-id="bde39-137">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde39-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="bde39-138">-UserId</span></span>
<span data-ttu-id="bde39-139">Anger användar-ID.</span><span class="sxs-lookup"><span data-stu-id="bde39-139">Specifies the user ID.</span></span>
<span data-ttu-id="bde39-140">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="bde39-140">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde39-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde39-141">CommonParameters</span></span>
<span data-ttu-id="bde39-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bde39-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde39-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bde39-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde39-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bde39-144">INPUTS</span></span>

### <span data-ttu-id="bde39-145">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bde39-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bde39-146">System. String</span><span class="sxs-lookup"><span data-stu-id="bde39-146">System.String</span></span>

### <span data-ttu-id="bde39-147">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="bde39-147">System.Security.SecureString</span></span>

### <span data-ttu-id="bde39-148">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="bde39-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="bde39-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bde39-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bde39-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bde39-150">OUTPUTS</span></span>

### <span data-ttu-id="bde39-151">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bde39-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="bde39-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bde39-152">NOTES</span></span>

## <span data-ttu-id="bde39-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bde39-153">RELATED LINKS</span></span>

[<span data-ttu-id="bde39-154">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bde39-154">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="bde39-155">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bde39-155">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="bde39-156">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bde39-156">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


