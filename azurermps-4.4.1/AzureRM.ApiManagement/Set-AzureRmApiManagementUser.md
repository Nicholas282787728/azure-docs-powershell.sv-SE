---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: a9d36dca9894a10c76f2ca5a96880f4aafecb5e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573749"
---
# <span data-ttu-id="2494f-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2494f-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="2494f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2494f-102">SYNOPSIS</span></span>
<span data-ttu-id="2494f-103">Anger användar information.</span><span class="sxs-lookup"><span data-stu-id="2494f-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2494f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2494f-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <String>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2494f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2494f-105">DESCRIPTION</span></span>
<span data-ttu-id="2494f-106">Cmdleten **set-AzureRmApiManagementUser** anger användar information.</span><span class="sxs-lookup"><span data-stu-id="2494f-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="2494f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2494f-107">EXAMPLES</span></span>

### <span data-ttu-id="2494f-108">Exempel 1: ändra en användares lösen ord, e-postadress och status</span><span class="sxs-lookup"><span data-stu-id="2494f-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password "asdfgh" -State "Blocked"
```

<span data-ttu-id="2494f-109">Det här kommandot anger ett nytt lösen ord och en e-postadress för användaren.</span><span class="sxs-lookup"><span data-stu-id="2494f-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="2494f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2494f-110">PARAMETERS</span></span>

### <span data-ttu-id="2494f-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2494f-111">-Context</span></span>
<span data-ttu-id="2494f-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2494f-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="2494f-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2494f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2494f-114">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="2494f-114">-Email</span></span>
<span data-ttu-id="2494f-115">Anger användarens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="2494f-115">Specifies the email address of the user.</span></span>
<span data-ttu-id="2494f-116">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="2494f-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="2494f-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="2494f-117">-FirstName</span></span>
<span data-ttu-id="2494f-118">Anger användarens förnamn.</span><span class="sxs-lookup"><span data-stu-id="2494f-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="2494f-119">Parametern måste vara 1 till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="2494f-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="2494f-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="2494f-120">-LastName</span></span>
<span data-ttu-id="2494f-121">Anger användarens efter namn.</span><span class="sxs-lookup"><span data-stu-id="2494f-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="2494f-122">Parametern måste vara 1 till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="2494f-122">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="2494f-123">-Obs!</span><span class="sxs-lookup"><span data-stu-id="2494f-123">-Note</span></span>
<span data-ttu-id="2494f-124">Anger en kommentar om användaren.</span><span class="sxs-lookup"><span data-stu-id="2494f-124">Specifies a note about the user.</span></span>
<span data-ttu-id="2494f-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="2494f-125">This parameter is optional.</span></span>
<span data-ttu-id="2494f-126">Standardvärdet för den här parametern är $null.</span><span class="sxs-lookup"><span data-stu-id="2494f-126">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="2494f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2494f-127">-PassThru</span></span>
<span data-ttu-id="2494f-128">passthru</span><span class="sxs-lookup"><span data-stu-id="2494f-128">passthru</span></span>

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

### <span data-ttu-id="2494f-129">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="2494f-129">-Password</span></span>
<span data-ttu-id="2494f-130">Anger användarens lösen ord.</span><span class="sxs-lookup"><span data-stu-id="2494f-130">Specifies the user password.</span></span>
<span data-ttu-id="2494f-131">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="2494f-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="2494f-132">-State</span><span class="sxs-lookup"><span data-stu-id="2494f-132">-State</span></span>
<span data-ttu-id="2494f-133">Anger användar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="2494f-133">Specifies the user state.</span></span>
<span data-ttu-id="2494f-134">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="2494f-134">This parameter is optional.</span></span>
<span data-ttu-id="2494f-135">Standardvärdet är aktivt.</span><span class="sxs-lookup"><span data-stu-id="2494f-135">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2494f-136">-UserId</span><span class="sxs-lookup"><span data-stu-id="2494f-136">-UserId</span></span>
<span data-ttu-id="2494f-137">Anger användar-ID.</span><span class="sxs-lookup"><span data-stu-id="2494f-137">Specifies the user ID.</span></span>
<span data-ttu-id="2494f-138">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2494f-138">This parameter is required.</span></span>

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

### <span data-ttu-id="2494f-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2494f-139">-DefaultProfile</span></span>
<span data-ttu-id="2494f-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2494f-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2494f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2494f-141">CommonParameters</span></span>
<span data-ttu-id="2494f-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2494f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2494f-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2494f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2494f-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2494f-144">INPUTS</span></span>

## <span data-ttu-id="2494f-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2494f-145">OUTPUTS</span></span>

### <span data-ttu-id="2494f-146">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2494f-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="2494f-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2494f-147">NOTES</span></span>

## <span data-ttu-id="2494f-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2494f-148">RELATED LINKS</span></span>

[<span data-ttu-id="2494f-149">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2494f-149">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="2494f-150">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2494f-150">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="2494f-151">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2494f-151">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


