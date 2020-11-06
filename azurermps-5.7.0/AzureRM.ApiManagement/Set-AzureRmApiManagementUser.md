---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: d3825b4887d2361a4bb378bfddc3085773efd84b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584479"
---
# <span data-ttu-id="1a0cd-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1a0cd-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="1a0cd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a0cd-102">SYNOPSIS</span></span>
<span data-ttu-id="1a0cd-103">Anger användar information.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a0cd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a0cd-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a0cd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a0cd-105">DESCRIPTION</span></span>
<span data-ttu-id="1a0cd-106">Cmdleten **set-AzureRmApiManagementUser** anger användar information.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="1a0cd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a0cd-107">EXAMPLES</span></span>

### <span data-ttu-id="1a0cd-108">Exempel 1: ändra en användares lösen ord, e-postadress och status</span><span class="sxs-lookup"><span data-stu-id="1a0cd-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="1a0cd-109">Det här kommandot anger ett nytt lösen ord och en e-postadress för användaren.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="1a0cd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a0cd-110">PARAMETERS</span></span>

### <span data-ttu-id="1a0cd-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="1a0cd-111">-Context</span></span>
<span data-ttu-id="1a0cd-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="1a0cd-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-113">This parameter is required.</span></span>

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

### <span data-ttu-id="1a0cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a0cd-114">-DefaultProfile</span></span>
<span data-ttu-id="1a0cd-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="1a0cd-116">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="1a0cd-116">-Email</span></span>
<span data-ttu-id="1a0cd-117">Anger användarens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="1a0cd-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-118">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0cd-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="1a0cd-119">-FirstName</span></span>
<span data-ttu-id="1a0cd-120">Anger användarens förnamn.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="1a0cd-121">Parametern måste vara 1 till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-121">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0cd-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="1a0cd-122">-LastName</span></span>
<span data-ttu-id="1a0cd-123">Anger användarens efter namn.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="1a0cd-124">Parametern måste vara 1 till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-124">This parameter is must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0cd-125">-Obs!</span><span class="sxs-lookup"><span data-stu-id="1a0cd-125">-Note</span></span>
<span data-ttu-id="1a0cd-126">Anger en kommentar om användaren.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-126">Specifies a note about the user.</span></span>
<span data-ttu-id="1a0cd-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-127">This parameter is optional.</span></span>
<span data-ttu-id="1a0cd-128">Standardvärdet för den här parametern är $null.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-128">The default value of this parameter is $null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0cd-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a0cd-129">-PassThru</span></span>
<span data-ttu-id="1a0cd-130">passthru</span><span class="sxs-lookup"><span data-stu-id="1a0cd-130">passthru</span></span>

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

### <span data-ttu-id="1a0cd-131">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="1a0cd-131">-Password</span></span>
<span data-ttu-id="1a0cd-132">Anger användarens lösen ord.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-132">Specifies the user password.</span></span>
<span data-ttu-id="1a0cd-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-133">This parameter is optional.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0cd-134">-State</span><span class="sxs-lookup"><span data-stu-id="1a0cd-134">-State</span></span>
<span data-ttu-id="1a0cd-135">Anger användar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-135">Specifies the user state.</span></span>
<span data-ttu-id="1a0cd-136">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-136">This parameter is optional.</span></span>
<span data-ttu-id="1a0cd-137">Standardvärdet är aktivt.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-137">The default value is Active.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0cd-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="1a0cd-138">-UserId</span></span>
<span data-ttu-id="1a0cd-139">Anger användar-ID.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-139">Specifies the user ID.</span></span>
<span data-ttu-id="1a0cd-140">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-140">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0cd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a0cd-141">CommonParameters</span></span>
<span data-ttu-id="1a0cd-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a0cd-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a0cd-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a0cd-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a0cd-144">INPUTS</span></span>

### <span data-ttu-id="1a0cd-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="1a0cd-145">None</span></span>
<span data-ttu-id="1a0cd-146">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1a0cd-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1a0cd-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a0cd-147">OUTPUTS</span></span>

### <span data-ttu-id="1a0cd-148">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1a0cd-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="1a0cd-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a0cd-149">NOTES</span></span>

## <span data-ttu-id="1a0cd-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a0cd-150">RELATED LINKS</span></span>

[<span data-ttu-id="1a0cd-151">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1a0cd-151">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="1a0cd-152">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1a0cd-152">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="1a0cd-153">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1a0cd-153">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


