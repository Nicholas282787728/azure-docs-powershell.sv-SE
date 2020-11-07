---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: 2867e8eec65de040a0da61a1af960abc9797bb18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756642"
---
# <span data-ttu-id="5df67-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="5df67-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="5df67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5df67-102">SYNOPSIS</span></span>
<span data-ttu-id="5df67-103">Tar bort en användare från en grupp.</span><span class="sxs-lookup"><span data-stu-id="5df67-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5df67-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5df67-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5df67-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5df67-105">DESCRIPTION</span></span>
<span data-ttu-id="5df67-106">Cmdleten **Remove-AzureRmApiManagementUserFromGroup** tar bort en användare från en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="5df67-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="5df67-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5df67-107">EXAMPLES</span></span>

### <span data-ttu-id="5df67-108">Exempel 1: ta bort en användare från en grupp</span><span class="sxs-lookup"><span data-stu-id="5df67-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="5df67-109">Det här kommandot tar bort en användare från en grupp.</span><span class="sxs-lookup"><span data-stu-id="5df67-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="5df67-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5df67-110">PARAMETERS</span></span>

### <span data-ttu-id="5df67-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="5df67-111">-Context</span></span>
<span data-ttu-id="5df67-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="5df67-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="5df67-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="5df67-113">This parameter is required.</span></span>

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

### <span data-ttu-id="5df67-114">-Kund-</span><span class="sxs-lookup"><span data-stu-id="5df67-114">-GroupId</span></span>
<span data-ttu-id="5df67-115">Anger ID för den grupp som du vill ta bort en användare från.</span><span class="sxs-lookup"><span data-stu-id="5df67-115">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="5df67-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5df67-116">-PassThru</span></span>
<span data-ttu-id="5df67-117">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="5df67-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="5df67-118">-UserId</span><span class="sxs-lookup"><span data-stu-id="5df67-118">-UserId</span></span>
<span data-ttu-id="5df67-119">Anger ID: t för den användare som ska tas bort från gruppen.</span><span class="sxs-lookup"><span data-stu-id="5df67-119">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="5df67-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df67-120">-DefaultProfile</span></span>
<span data-ttu-id="5df67-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5df67-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5df67-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df67-122">CommonParameters</span></span>
<span data-ttu-id="5df67-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5df67-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df67-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5df67-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df67-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5df67-125">INPUTS</span></span>

## <span data-ttu-id="5df67-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5df67-126">OUTPUTS</span></span>

### <span data-ttu-id="5df67-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5df67-127">System.Boolean</span></span>

## <span data-ttu-id="5df67-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5df67-128">NOTES</span></span>

## <span data-ttu-id="5df67-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5df67-129">RELATED LINKS</span></span>

[<span data-ttu-id="5df67-130">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="5df67-130">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="5df67-131">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5df67-131">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


