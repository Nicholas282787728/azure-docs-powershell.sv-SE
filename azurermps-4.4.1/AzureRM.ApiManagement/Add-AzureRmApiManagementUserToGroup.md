---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: d405dc21719abc1aec5767f4d1b89a938b79eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575059"
---
# <span data-ttu-id="6d4bc-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="6d4bc-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="6d4bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d4bc-102">SYNOPSIS</span></span>
<span data-ttu-id="6d4bc-103">Lägger till en användare i en grupp.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d4bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d4bc-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d4bc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d4bc-105">DESCRIPTION</span></span>
<span data-ttu-id="6d4bc-106">Cmdleten **Add-AzureRmApiManagementUserToGroup** lägger till en användare i en grupp.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="6d4bc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d4bc-107">EXAMPLES</span></span>

### <span data-ttu-id="6d4bc-108">Exempel 1: lägga till en användare i en grupp</span><span class="sxs-lookup"><span data-stu-id="6d4bc-108">Example 1: Add a user to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="6d4bc-109">Det här kommandot lägger till en befintlig användare i en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="6d4bc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d4bc-110">PARAMETERS</span></span>

### <span data-ttu-id="6d4bc-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6d4bc-111">-Context</span></span>
<span data-ttu-id="6d4bc-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="6d4bc-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6d4bc-114">-Kund-</span><span class="sxs-lookup"><span data-stu-id="6d4bc-114">-GroupId</span></span>
<span data-ttu-id="6d4bc-115">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-115">Specifies the group ID.</span></span>
<span data-ttu-id="6d4bc-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-116">This parameter is required.</span></span>

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

### <span data-ttu-id="6d4bc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d4bc-117">-PassThru</span></span>
<span data-ttu-id="6d4bc-118">passthru</span><span class="sxs-lookup"><span data-stu-id="6d4bc-118">passthru</span></span>

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

### <span data-ttu-id="6d4bc-119">-UserId</span><span class="sxs-lookup"><span data-stu-id="6d4bc-119">-UserId</span></span>
<span data-ttu-id="6d4bc-120">Anger användar-ID.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-120">Specifies the user ID.</span></span>
<span data-ttu-id="6d4bc-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-121">This parameter is required.</span></span>

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

### <span data-ttu-id="6d4bc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d4bc-122">-DefaultProfile</span></span>
<span data-ttu-id="6d4bc-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d4bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d4bc-124">CommonParameters</span></span>
<span data-ttu-id="6d4bc-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d4bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d4bc-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d4bc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d4bc-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d4bc-127">INPUTS</span></span>

## <span data-ttu-id="6d4bc-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d4bc-128">OUTPUTS</span></span>

### <span data-ttu-id="6d4bc-129">Returtyp</span><span class="sxs-lookup"><span data-stu-id="6d4bc-129">Boolean</span></span>

## <span data-ttu-id="6d4bc-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d4bc-130">NOTES</span></span>

## <span data-ttu-id="6d4bc-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d4bc-131">RELATED LINKS</span></span>

[<span data-ttu-id="6d4bc-132">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="6d4bc-132">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="6d4bc-133">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="6d4bc-133">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


