---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 030a5ed61b4faafb47e8cba808dada484180a01c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758274"
---
# <span data-ttu-id="9f6c3-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="9f6c3-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="9f6c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f6c3-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6c3-103">Tar bort en Azure AD-administratör för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9f6c3-103">Removes an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f6c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f6c3-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f6c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f6c3-105">DESCRIPTION</span></span>
<span data-ttu-id="9f6c3-106">Cmdleten **Remove-AzureRmSqlServerActiveDirectoryAdministrator** tar bort en Azure Active Directory (Azure AD-administratör) för AzureSQL-servern i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9f6c3-106">The **Remove-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="9f6c3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f6c3-107">EXAMPLES</span></span>

### <span data-ttu-id="9f6c3-108">Exempel 1: ta bort en administratör</span><span class="sxs-lookup"><span data-stu-id="9f6c3-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="9f6c3-109">Det här kommandot tar bort Azure AD-administratören för servern som heter Server01 associerad med resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="9f6c3-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="9f6c3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f6c3-110">PARAMETERS</span></span>

### <span data-ttu-id="9f6c3-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9f6c3-111">-Force</span></span>
<span data-ttu-id="9f6c3-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9f6c3-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6c3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f6c3-113">-ResourceGroupName</span></span>
<span data-ttu-id="9f6c3-114">Anger namnet på den resurs grupp som SQL-servern har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="9f6c3-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f6c3-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9f6c3-115">-ServerName</span></span>
<span data-ttu-id="9f6c3-116">Anger namnet på den SQL Server för vilken denna cmdlet tar bort en administratör.</span><span class="sxs-lookup"><span data-stu-id="9f6c3-116">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f6c3-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9f6c3-117">-Confirm</span></span>
<span data-ttu-id="9f6c3-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9f6c3-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6c3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f6c3-119">-WhatIf</span></span>
<span data-ttu-id="9f6c3-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9f6c3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f6c3-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9f6c3-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f6c3-122">-DefaultProfile</span></span>
<span data-ttu-id="9f6c3-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f6c3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f6c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6c3-124">CommonParameters</span></span>
<span data-ttu-id="9f6c3-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f6c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6c3-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f6c3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6c3-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f6c3-127">INPUTS</span></span>

### <span data-ttu-id="9f6c3-128">Microsoft. Azure. commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="9f6c3-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="9f6c3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f6c3-129">OUTPUTS</span></span>

### <span data-ttu-id="9f6c3-130">Microsoft. Azure. commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="9f6c3-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="9f6c3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f6c3-131">NOTES</span></span>

## <span data-ttu-id="9f6c3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f6c3-132">RELATED LINKS</span></span>

[<span data-ttu-id="9f6c3-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="9f6c3-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="9f6c3-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="9f6c3-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="9f6c3-135">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="9f6c3-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

