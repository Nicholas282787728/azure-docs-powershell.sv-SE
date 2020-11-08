---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090287"
---
# <span data-ttu-id="f00a1-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="f00a1-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="f00a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f00a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f00a1-103">Skapa en ny instans DataMigration för Azure ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="f00a1-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="f00a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f00a1-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f00a1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f00a1-105">DESCRIPTION</span></span>
<span data-ttu-id="f00a1-106">Skapa en ny instans DataMigration för Azure ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="f00a1-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="f00a1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f00a1-107">EXAMPLES</span></span>

### <span data-ttu-id="f00a1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f00a1-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="f00a1-109">ApplicationId: "ditt huvud program för AppId/service här" AppKey: system. Security. SecureString TenantId: "klient-ID"</span><span class="sxs-lookup"><span data-stu-id="f00a1-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="f00a1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f00a1-110">PARAMETERS</span></span>

### <span data-ttu-id="f00a1-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="f00a1-111">-AppKey</span></span>
<span data-ttu-id="f00a1-112">Azure Active Directory-register</span><span class="sxs-lookup"><span data-stu-id="f00a1-112">Azure Active Directory Key</span></span>

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

### <span data-ttu-id="f00a1-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f00a1-113">-ApplicationId</span></span>
<span data-ttu-id="f00a1-114">ID för Azure Active Directory-programmet</span><span class="sxs-lookup"><span data-stu-id="f00a1-114">Azure Active Directory Application Id</span></span>

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

### <span data-ttu-id="f00a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f00a1-115">-DefaultProfile</span></span>
<span data-ttu-id="f00a1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f00a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f00a1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f00a1-117">CommonParameters</span></span>
<span data-ttu-id="f00a1-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f00a1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f00a1-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f00a1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f00a1-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f00a1-120">INPUTS</span></span>

### <span data-ttu-id="f00a1-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="f00a1-121">None</span></span>

## <span data-ttu-id="f00a1-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f00a1-122">OUTPUTS</span></span>

### <span data-ttu-id="f00a1-123">Microsoft. Azure. commands. DataMigration. Models. PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="f00a1-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="f00a1-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f00a1-124">NOTES</span></span>

## <span data-ttu-id="f00a1-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f00a1-125">RELATED LINKS</span></span>