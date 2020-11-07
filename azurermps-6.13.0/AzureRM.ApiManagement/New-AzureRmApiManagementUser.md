---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 1c8b7f8069c63d18f69285f7e40ac4d652f0bf73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755727"
---
# <span data-ttu-id="9ce5e-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9ce5e-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="9ce5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ce5e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce5e-103">Registrerar en ny användare.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ce5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ce5e-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ce5e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ce5e-105">DESCRIPTION</span></span>
<span data-ttu-id="9ce5e-106">**New-AzureRmApiManagementUser-** cmdleten registrerar en ny användare.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="9ce5e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ce5e-107">EXAMPLES</span></span>

### <span data-ttu-id="9ce5e-108">Exempel 1: registrera en ny användare</span><span class="sxs-lookup"><span data-stu-id="9ce5e-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="9ce5e-109">Det här kommandot registrerar en ny användare som heter Patti Nilsson.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="9ce5e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ce5e-110">PARAMETERS</span></span>

### <span data-ttu-id="9ce5e-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="9ce5e-111">-Context</span></span>
<span data-ttu-id="9ce5e-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9ce5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ce5e-113">-DefaultProfile</span></span>
<span data-ttu-id="9ce5e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ce5e-115">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="9ce5e-115">-Email</span></span>
<span data-ttu-id="9ce5e-116">Anger användarens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="9ce5e-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="9ce5e-117">-FirstName</span></span>
<span data-ttu-id="9ce5e-118">Anger användarens förnamn.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="9ce5e-119">Parametern måste vara 1 till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="9ce5e-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="9ce5e-120">-LastName</span></span>
<span data-ttu-id="9ce5e-121">Anger användarens efter namn.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="9ce5e-122">Parametern måste vara 1 till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="9ce5e-123">-Obs!</span><span class="sxs-lookup"><span data-stu-id="9ce5e-123">-Note</span></span>
<span data-ttu-id="9ce5e-124">Anger en kommentar om användaren.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-124">Specifies a note about the user.</span></span>
<span data-ttu-id="9ce5e-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-125">This parameter is optional.</span></span>
<span data-ttu-id="9ce5e-126">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="9ce5e-127">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="9ce5e-127">-Password</span></span>
<span data-ttu-id="9ce5e-128">Anger användarens lösen ord.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-128">Specifies the user password.</span></span>
<span data-ttu-id="9ce5e-129">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-129">This parameter is required.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ce5e-130">-State</span><span class="sxs-lookup"><span data-stu-id="9ce5e-130">-State</span></span>
<span data-ttu-id="9ce5e-131">Anger användar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-131">Specifies the user state.</span></span>
<span data-ttu-id="9ce5e-132">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-132">This parameter is optional.</span></span>
<span data-ttu-id="9ce5e-133">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ce5e-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="9ce5e-134">-UserId</span></span>
<span data-ttu-id="9ce5e-135">Anger användar-ID.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-135">Specifies the user ID.</span></span>
<span data-ttu-id="9ce5e-136">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-136">This parameter is optional.</span></span>
<span data-ttu-id="9ce5e-137">Om den här parametern inte anges skapar den här cmdleten ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="9ce5e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce5e-138">CommonParameters</span></span>
<span data-ttu-id="9ce5e-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ce5e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce5e-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ce5e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce5e-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ce5e-141">INPUTS</span></span>

### <span data-ttu-id="9ce5e-142">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9ce5e-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9ce5e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9ce5e-143">System.String</span></span>

### <span data-ttu-id="9ce5e-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="9ce5e-144">System.Security.SecureString</span></span>

### <span data-ttu-id="9ce5e-145">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState, Microsoft. Azure. commands. ApiManagement. ServiceManagement, version = 6.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9ce5e-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9ce5e-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ce5e-146">OUTPUTS</span></span>

### <span data-ttu-id="9ce5e-147">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9ce5e-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="9ce5e-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ce5e-148">NOTES</span></span>

## <span data-ttu-id="9ce5e-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ce5e-149">RELATED LINKS</span></span>

[<span data-ttu-id="9ce5e-150">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9ce5e-150">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="9ce5e-151">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9ce5e-151">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


