---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260017"
---
# <span data-ttu-id="a01ed-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="a01ed-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="a01ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a01ed-102">SYNOPSIS</span></span>
<span data-ttu-id="a01ed-103">Skapa en ny instans DataMigration för Azure ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="a01ed-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="a01ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a01ed-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a01ed-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a01ed-105">DESCRIPTION</span></span>
<span data-ttu-id="a01ed-106">Skapa en ny instans DataMigration för Azure ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="a01ed-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="a01ed-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a01ed-107">EXAMPLES</span></span>

### <span data-ttu-id="a01ed-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a01ed-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="a01ed-109">ApplicationId: "ditt huvud program för AppId/service här" AppKey: system. Security. SecureString TenantId: "klient-ID"</span><span class="sxs-lookup"><span data-stu-id="a01ed-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="a01ed-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a01ed-110">PARAMETERS</span></span>

### <span data-ttu-id="a01ed-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="a01ed-111">-AppKey</span></span>
<span data-ttu-id="a01ed-112">Azure Active Directory-register</span><span class="sxs-lookup"><span data-stu-id="a01ed-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a01ed-113">-ApplicationId</span></span>
<span data-ttu-id="a01ed-114">ID för Azure Active Directory-programmet</span><span class="sxs-lookup"><span data-stu-id="a01ed-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a01ed-115">-DefaultProfile</span></span>
<span data-ttu-id="a01ed-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a01ed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a01ed-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01ed-117">CommonParameters</span></span>
<span data-ttu-id="a01ed-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a01ed-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a01ed-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a01ed-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01ed-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a01ed-120">INPUTS</span></span>

### <span data-ttu-id="a01ed-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="a01ed-121">None</span></span>

## <span data-ttu-id="a01ed-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a01ed-122">OUTPUTS</span></span>

### <span data-ttu-id="a01ed-123">Microsoft. Azure. commands. DataMigration. Models. PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="a01ed-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="a01ed-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a01ed-124">NOTES</span></span>

## <span data-ttu-id="a01ed-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a01ed-125">RELATED LINKS</span></span>
