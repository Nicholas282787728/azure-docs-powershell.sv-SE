---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 2d7a7d61d5a29113f9b0e40340ae6b13b599115f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744508"
---
# <span data-ttu-id="83d51-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="83d51-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="83d51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83d51-102">SYNOPSIS</span></span>
<span data-ttu-id="83d51-103">Skapa en ny instans DataMigration för Azure ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="83d51-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="83d51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83d51-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83d51-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83d51-105">DESCRIPTION</span></span>
<span data-ttu-id="83d51-106">Skapa en ny instans DataMigration för Azure ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="83d51-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="83d51-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83d51-107">EXAMPLES</span></span>

### <span data-ttu-id="83d51-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="83d51-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="83d51-109">ApplicationId: "ditt huvud program för AppId/service här" AppKey: system. Security. SecureString TenantId: "klient-ID"</span><span class="sxs-lookup"><span data-stu-id="83d51-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="83d51-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83d51-110">PARAMETERS</span></span>

### <span data-ttu-id="83d51-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="83d51-111">-AppKey</span></span>
<span data-ttu-id="83d51-112">Azure Active Directory-register</span><span class="sxs-lookup"><span data-stu-id="83d51-112">Azure Active Directory Key</span></span>

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

### <span data-ttu-id="83d51-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="83d51-113">-ApplicationId</span></span>
<span data-ttu-id="83d51-114">ID för Azure Active Directory-programmet</span><span class="sxs-lookup"><span data-stu-id="83d51-114">Azure Active Directory Application Id</span></span>

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

### <span data-ttu-id="83d51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d51-115">-DefaultProfile</span></span>
<span data-ttu-id="83d51-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83d51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83d51-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d51-117">CommonParameters</span></span>
<span data-ttu-id="83d51-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d51-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="83d51-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83d51-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d51-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83d51-120">INPUTS</span></span>

### <span data-ttu-id="83d51-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="83d51-121">None</span></span>

## <span data-ttu-id="83d51-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83d51-122">OUTPUTS</span></span>

### <span data-ttu-id="83d51-123">Microsoft. Azure. commands. DataMigration. Models. PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="83d51-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="83d51-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83d51-124">NOTES</span></span>

## <span data-ttu-id="83d51-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83d51-125">RELATED LINKS</span></span>
