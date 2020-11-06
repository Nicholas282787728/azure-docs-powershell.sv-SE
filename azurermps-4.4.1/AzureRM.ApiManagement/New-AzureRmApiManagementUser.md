---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 93e6ce5a96afd1c3b297d6296c3491445593d430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579859"
---
# <span data-ttu-id="40c87-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="40c87-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="40c87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40c87-102">SYNOPSIS</span></span>
<span data-ttu-id="40c87-103">Registrerar en ny användare.</span><span class="sxs-lookup"><span data-stu-id="40c87-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40c87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40c87-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <String> [-State <PsApiManagementUserState>] [-Note <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40c87-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40c87-105">DESCRIPTION</span></span>
<span data-ttu-id="40c87-106">**New-AzureRmApiManagementUser-** cmdleten registrerar en ny användare.</span><span class="sxs-lookup"><span data-stu-id="40c87-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="40c87-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40c87-107">EXAMPLES</span></span>

### <span data-ttu-id="40c87-108">Exempel 1: registrera en ny användare</span><span class="sxs-lookup"><span data-stu-id="40c87-108">Example 1: Register a new user</span></span>
```
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password "qwerty"
```

<span data-ttu-id="40c87-109">Det här kommandot registrerar en ny användare som heter Patti Nilsson.</span><span class="sxs-lookup"><span data-stu-id="40c87-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="40c87-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40c87-110">PARAMETERS</span></span>

### <span data-ttu-id="40c87-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="40c87-111">-Context</span></span>
<span data-ttu-id="40c87-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="40c87-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="40c87-113">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="40c87-113">-Email</span></span>
<span data-ttu-id="40c87-114">Anger användarens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="40c87-114">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="40c87-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="40c87-115">-FirstName</span></span>
<span data-ttu-id="40c87-116">Anger användarens förnamn.</span><span class="sxs-lookup"><span data-stu-id="40c87-116">Specifies the first name of the user.</span></span>
<span data-ttu-id="40c87-117">Parametern måste vara 1 till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="40c87-117">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="40c87-118">-LastName</span><span class="sxs-lookup"><span data-stu-id="40c87-118">-LastName</span></span>
<span data-ttu-id="40c87-119">Anger användarens efter namn.</span><span class="sxs-lookup"><span data-stu-id="40c87-119">Specifies the last name of the user.</span></span>
<span data-ttu-id="40c87-120">Parametern måste vara 1 till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="40c87-120">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="40c87-121">-Obs!</span><span class="sxs-lookup"><span data-stu-id="40c87-121">-Note</span></span>
<span data-ttu-id="40c87-122">Anger en kommentar om användaren.</span><span class="sxs-lookup"><span data-stu-id="40c87-122">Specifies a note about the user.</span></span>
<span data-ttu-id="40c87-123">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="40c87-123">This parameter is optional.</span></span>
<span data-ttu-id="40c87-124">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="40c87-124">The default value is $Null.</span></span>

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

### <span data-ttu-id="40c87-125">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="40c87-125">-Password</span></span>
<span data-ttu-id="40c87-126">Anger användarens lösen ord.</span><span class="sxs-lookup"><span data-stu-id="40c87-126">Specifies the user password.</span></span>
<span data-ttu-id="40c87-127">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="40c87-127">This parameter is required.</span></span>

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

### <span data-ttu-id="40c87-128">-State</span><span class="sxs-lookup"><span data-stu-id="40c87-128">-State</span></span>
<span data-ttu-id="40c87-129">Anger användar tillståndet.</span><span class="sxs-lookup"><span data-stu-id="40c87-129">Specifies the user state.</span></span>
<span data-ttu-id="40c87-130">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="40c87-130">This parameter is optional.</span></span>
<span data-ttu-id="40c87-131">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="40c87-131">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c87-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="40c87-132">-UserId</span></span>
<span data-ttu-id="40c87-133">Anger användar-ID.</span><span class="sxs-lookup"><span data-stu-id="40c87-133">Specifies the user ID.</span></span>
<span data-ttu-id="40c87-134">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="40c87-134">This parameter is optional.</span></span>
<span data-ttu-id="40c87-135">Om den här parametern inte anges skapar den här cmdleten ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="40c87-135">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="40c87-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c87-136">-DefaultProfile</span></span>
<span data-ttu-id="40c87-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40c87-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40c87-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c87-138">CommonParameters</span></span>
<span data-ttu-id="40c87-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40c87-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c87-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40c87-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c87-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40c87-141">INPUTS</span></span>

## <span data-ttu-id="40c87-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40c87-142">OUTPUTS</span></span>

### <span data-ttu-id="40c87-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="40c87-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="40c87-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40c87-144">NOTES</span></span>

## <span data-ttu-id="40c87-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40c87-145">RELATED LINKS</span></span>

[<span data-ttu-id="40c87-146">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="40c87-146">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="40c87-147">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="40c87-147">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


