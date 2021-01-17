---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 4fcceb8c268f025ac3898ebf01f5b77a9bab54a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416224"
---
# <span data-ttu-id="bc296-101">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="bc296-101">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="bc296-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bc296-102">SYNOPSIS</span></span>
<span data-ttu-id="bc296-103">Tar bort en Azure AD-administratör för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bc296-103">Removes an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="bc296-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bc296-104">SYNTAX</span></span>

```
Remove-AzSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc296-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bc296-105">DESCRIPTION</span></span>
<span data-ttu-id="bc296-106">Cmdleten **Remove-AzSqlServerActiveDirectoryAdministrator** tar bort en Azure Active Directory (Azure AD-administratör) för AzureSQL-servern i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="bc296-106">The **Remove-AzSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="bc296-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bc296-107">EXAMPLES</span></span>

### <span data-ttu-id="bc296-108">Exempel 1: ta bort en administratör</span><span class="sxs-lookup"><span data-stu-id="bc296-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="bc296-109">Det här kommandot tar bort Azure AD-administratören för servern som heter Server01 associerad med resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="bc296-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="bc296-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bc296-110">PARAMETERS</span></span>

### <span data-ttu-id="bc296-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc296-111">-DefaultProfile</span></span>
<span data-ttu-id="bc296-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bc296-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc296-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bc296-113">-Force</span></span>
<span data-ttu-id="bc296-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="bc296-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bc296-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc296-115">-ResourceGroupName</span></span>
<span data-ttu-id="bc296-116">Anger namnet på den resurs grupp som SQL-servern har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="bc296-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="bc296-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bc296-117">-ServerName</span></span>
<span data-ttu-id="bc296-118">Anger namnet på den SQL Server för vilken denna cmdlet tar bort en administratör.</span><span class="sxs-lookup"><span data-stu-id="bc296-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="bc296-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bc296-119">-Confirm</span></span>
<span data-ttu-id="bc296-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bc296-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc296-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc296-121">-WhatIf</span></span>
<span data-ttu-id="bc296-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bc296-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc296-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bc296-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc296-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc296-124">CommonParameters</span></span>
<span data-ttu-id="bc296-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc296-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc296-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc296-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc296-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bc296-127">INPUTS</span></span>

### <span data-ttu-id="bc296-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bc296-128">System.String</span></span>

## <span data-ttu-id="bc296-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bc296-129">OUTPUTS</span></span>

### <span data-ttu-id="bc296-130">Microsoft. Azure. commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="bc296-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="bc296-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bc296-131">NOTES</span></span>

## <span data-ttu-id="bc296-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bc296-132">RELATED LINKS</span></span>

[<span data-ttu-id="bc296-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="bc296-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="bc296-134">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="bc296-134">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="bc296-135">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="bc296-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


