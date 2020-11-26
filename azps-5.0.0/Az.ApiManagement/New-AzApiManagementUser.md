---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 6cc922ceb09509e70a4017241dc6beb6e5443d1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272966"
---
# <span data-ttu-id="bfff9-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bfff9-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="bfff9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bfff9-102">SYNOPSIS</span></span>
<span data-ttu-id="bfff9-103">Registrerar en ny användare.</span><span class="sxs-lookup"><span data-stu-id="bfff9-103">Registers a new user.</span></span>

## <span data-ttu-id="bfff9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bfff9-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfff9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bfff9-105">DESCRIPTION</span></span>
<span data-ttu-id="bfff9-106">**New-AzApiManagementUser-** cmdleten registrerar en ny användare.</span><span class="sxs-lookup"><span data-stu-id="bfff9-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="bfff9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bfff9-107">EXAMPLES</span></span>

### <span data-ttu-id="bfff9-108">Exempel 1: registrera en ny användare</span><span class="sxs-lookup"><span data-stu-id="bfff9-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="bfff9-109">Det här kommandot registrerar en ny användare som heter Patti Nilsson.</span><span class="sxs-lookup"><span data-stu-id="bfff9-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="bfff9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bfff9-110">PARAMETERS</span></span>

### <span data-ttu-id="bfff9-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="bfff9-111">-Context</span></span>
<span data-ttu-id="bfff9-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bfff9-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bfff9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfff9-113">-DefaultProfile</span></span>
<span data-ttu-id="bfff9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bfff9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfff9-115">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="bfff9-115">-Email</span></span>
<span data-ttu-id="bfff9-116">Anger användarens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="bfff9-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="bfff9-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="bfff9-117">-FirstName</span></span>
<span data-ttu-id="bfff9-118">Anger användarens förnamn.</span><span class="sxs-lookup"><span data-stu-id="bfff9-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="bfff9-119">Parametern måste vara 1 till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="bfff9-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="bfff9-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="bfff9-120">-LastName</span></span>
<span data-ttu-id="bfff9-121">Anger användarens efter namn.</span><span class="sxs-lookup"><span data-stu-id="bfff9-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="bfff9-122">Parametern måste vara 1 till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="bfff9-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="bfff9-123">-Obs!</span><span class="sxs-lookup"><span data-stu-id="bfff9-123">-Note</span></span>
<span data-ttu-id="bfff9-124">Anger en kommentar om användaren.</span><span class="sxs-lookup"><span data-stu-id="bfff9-124">Specifies a note about the user.</span></span>
<span data-ttu-id="bfff9-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="bfff9-125">This parameter is optional.</span></span>
<span data-ttu-id="bfff9-126">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="bfff9-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="bfff9-127">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="bfff9-127">-Password</span></span>
<span data-ttu-id="bfff9-128">Anger användarens lösen ord.</span><span class="sxs-lookup"><span data-stu-id="bfff9-128">Specifies the user password.</span></span>
<span data-ttu-id="bfff9-129">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="bfff9-129">This parameter is required.</span></span>

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

### <span data-ttu-id="bfff9-130">-State</span><span class="sxs-lookup"><span data-stu-id="bfff9-130">-State</span></span>
<span data-ttu-id="bfff9-131">Anger användar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="bfff9-131">Specifies the user state.</span></span>
<span data-ttu-id="bfff9-132">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="bfff9-132">This parameter is optional.</span></span>
<span data-ttu-id="bfff9-133">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="bfff9-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="bfff9-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="bfff9-134">-UserId</span></span>
<span data-ttu-id="bfff9-135">Anger användar-ID.</span><span class="sxs-lookup"><span data-stu-id="bfff9-135">Specifies the user ID.</span></span>
<span data-ttu-id="bfff9-136">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="bfff9-136">This parameter is optional.</span></span>
<span data-ttu-id="bfff9-137">Om den här parametern inte anges skapar den här cmdleten ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="bfff9-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="bfff9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfff9-138">CommonParameters</span></span>
<span data-ttu-id="bfff9-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfff9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfff9-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfff9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfff9-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bfff9-141">INPUTS</span></span>

### <span data-ttu-id="bfff9-142">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bfff9-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bfff9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bfff9-143">System.String</span></span>

### <span data-ttu-id="bfff9-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="bfff9-144">System.Security.SecureString</span></span>

### <span data-ttu-id="bfff9-145">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState, Microsoft. Azure. PowerShell. cmdletar. ApiManagement. ServiceManagement, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bfff9-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bfff9-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bfff9-146">OUTPUTS</span></span>

### <span data-ttu-id="bfff9-147">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bfff9-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="bfff9-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bfff9-148">NOTES</span></span>

## <span data-ttu-id="bfff9-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bfff9-149">RELATED LINKS</span></span>

[<span data-ttu-id="bfff9-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bfff9-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="bfff9-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bfff9-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)

